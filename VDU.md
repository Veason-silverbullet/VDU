# Visual Document Understanding

## Previous Works

|Model       |Inputs                        |Model                                       |Objectives                                     |Abstract                                                                                      |
|------------|------------------------------|--------------------------------------------|-----------------------------------------------|----------------------------------------------------------------------------------------------|
|DONUT       |Image(patch)                  |Encoder-decoder Transformer                 |LM loss                                        |OCR-free visual document directly to text output                                              |
|LayoutLM-v1 |Image(ROI), Text, Layout      |BERT-architecture                           |MLM loss + Doc cls loss                        |The first layout pretranined model                                                            |
|LayoutLM-v2 |Image(ROI), Text, Layout      |BERT-architecture + relative bias attention |MLM loss + TIA loss + TIM loss                 |Multi-modal feature fusion, positional attention, alignment with multi-loss                   |
|LayoutLM-v3 |Image(patch), Text, Layout    |BEiT-architecture                           |MLM loss + MIM loss + WPA loss                 |Unifying masked language/image modeling, and binary CE alignment loss                         |
|SelfDoc     |Image(ROI), Text, Layout      |Two-tower Encoders + cross attention        |Masked VL Feature Reconstruction               |Two-tower single-modal modeling, then crosss-modal modeling, and finetune adaptation          |
|UniDoc      |Image(ROI), Text, Layout      |Single-tower Encoder + gated cross attention|Masked Language Feature Reconstruction + VL contrastive loss + VL aligment loss|Single-tower cross-interaction, contrastive and alignment loss|
|LiLT        ||||
|DocFormer   ||||
|ERNIE-Layout||||
|XDoc        |Plain, Document, and Web Texts|BERT-architecture                           |MLM loss                                       |Three input text formats(tasks), shared embedding and transformer layers, adaptive embedding  |
|BROS        |Image(ROI), Text, Layout      |BERT-architecture                           |MLM loss + Masked Area Modeling (SpanBERT)     |2D relative positional biases and area-masked language modeling                               |
|UDOP        |Image(patch), Text, Layout    |Multimodal encoder and prompt-based decoder |Maksed token modeling (SSL) + Supervised tasks |Multimodal encoder + multitask prompt-based decoder. Masked multi-modality modelings (masked language/layout/fusion/image modeling) and varied supervised tasks (DocCLS, DocVQA, LayoutAnalysis, IE, NLI)|
