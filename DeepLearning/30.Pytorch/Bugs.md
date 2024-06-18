> 'lengths' argument should be a 1D CPU int64 tensor, but got 1D cuda:0 Long tensor

在使用bilstm的时候报错

原因是pytorch版本太高了，在定义模型的前向传播的pack_padded_sequence时候需要将lengths改为cpu上的。

```python
# 用于文本情感分析的LSTM
class SentimentBiLSTM(nn.Module):
    def __init__(self, vocab_size, embedding_dim, hidden_dim, 
                 output_dim, n_layers, bidirectional, dropout, pad_idx):
        # ...
    
    def forward(self, text, text_lengths):
        embedded = self.dropout(self.embedding(text))
        # ===以下这行，text_lengths改为cpu上运行=====
        packed_embedded = nn.utils.rnn.pack_padded_sequence(embedded, text_lengths.to('cpu'), batch_first=True, enforce_sorted=False)
        packed_output, (hidden, cell) = self.bilstm(packed_embedded)
        hidden = self.dropout(torch.cat((hidden[-2,:,:], hidden[-1,:,:]), dim=1))
        return self.fc(hidden)
```