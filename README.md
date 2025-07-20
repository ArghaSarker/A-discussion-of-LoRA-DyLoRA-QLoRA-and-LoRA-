# A-discussion-of-LoRA-DyLoRA-QLoRA-and-LoRA-

Context
Pre-trained Large Language Models (LLMs) often contain large parameter matrices, e.g. query (Wq), key (Wk), and value (Wv) matrices in a Transformerbased model. In full fine-tuning, all parameters of such a pre-trained model are
considered, and this is for multiple epochs. This high training cost can only be
covered by the big companies.
Parameter-efficient fine-tuning (PEFT) methods aim to increase the accessibility of LLM fine-tuning by making it more cost-efficient, while maintaining
a performance comparable to full fine-tuning. Low-Rank Adaption (LoRA)
and its variants fall into the ’Reparameterized Fine-tuning’ category of PEFT,
i.e. the number of trainable parameters is reduced via low-rank transformation
on the large weight matrices.[1]
There are various PEFT methods developed already. This project report discusses LoRA[2], and three LoRA variants (DyLoRA[3], QLoRA[4], and LoRA+[5])
that each cover an essential limitation of vanilla LoRA. Figure 1 gives an
overview of the variants discussed in this project report.
