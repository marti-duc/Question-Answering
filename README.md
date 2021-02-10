# Question-Answering


Recently, Transformer-based models such as BERT have achieved state of the art performance on a variety of natural language tasks.  One such task is extractive question answering (QA), which involves extraction of text snippets from a given text passage that answers a given user question.  Among the many useful applications of such a system is answering the general public’s questions about the COVID-19 epidemic.  In this work, we explore the use of BERT for this application.  We introduce a hand-annotated dataset of 399 question-answer pairs collected from New Jersey’s COVID-19 Information Hub website.  When we evaluate a BERT QA model on this task that is trained on the popular open domain Stanford Question Answering Dataset (SQuAD), we find problems due to domain mismatch.  For example, some questions in our COVID data cannot be answered using just one span of text and many questions have multiple possible answers within the given text passage.  Furthermore, while SQuAD questions typically are answerable using noun phrases, COVID answers more often require clauses.  Consequently, we develop our own QA system for answering COVID questions.  It includes an answer selection model to pair the given question with its relevant text passage, and an answer extraction model to find the relevant text snippets within the text passage.  The models are developed by fine-tuning a base BERT model, using mixtures of SQuAD data and our own COVID data.
