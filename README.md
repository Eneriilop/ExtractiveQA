# Abstract
 This project aims to implement an extractive Question Answering (QA) system
 utilizing Wikipedia passages as the information source. Given a question and a
 relevant paragraph (i.e., the context) containing the answer, the model is expected
 to accurately identify and return the text span most likely to contain the answer.
 Weprimarily employed BERT-base models, recognized for their effectiveness in
 context analysis and their robustness as a baseline in the field. Our methodology
 leveraged the Hugging Face library, utilizing "fast" tokenizers to optimize perfor
mance and the accuracy of offset mapping. The experimental analysis involved
 fine-tuning BERT, ALBERT, and SpanBERT on the SQuAD 1.1 and SQuAD 2.0
 datasets. We developed a preprocessing phase to handle tokenization and context
 chunking, and a postprocessing phase to analyze model predictions, converting
 logits into text spans. For SQuAD 2.0, we implemented specific handling for
 unanswerable questions by comparing the best span’s score with that of the [CLS]
 token to determine a "no-answer" prediction. Our evaluation functions for SQuAD
 2.0 were custom-implemented due to issues with standard functions not properly
 recognizing our method for marking unanswerable questions. The results obtained
 on SQuAD 1.1 and SQuAD 2.0 are largely consistent with existing literature,
 despite minor variations attributable to the use of "base" model configurations (e.g.,
 for SpanBERT, which was "base" instead of "large" in reference papers) and the
 specific dataset splitting (less training data due to split). ALBERT and SpanBERT
 consistently demonstrated superior performance compared to BERT, confirming
 the effectiveness of these more recent architectures. This study underscores the
 continued relevance of transformer-based models for extractive QA and provides
 comparative insights into their performance under various dataset conditions
