## STS-b-context
### This is a modification to the STS-b dataset 
   More Details regarding the original STS-b dataset can be found under the below citation
   
   Eneko Agirre, Daniel Cer, Mona Diab, Iñigo Lopez-Gazpio, Lucia
    Specia. Semeval-2017 Task 1: Semantic Textual Similarity
    Multilingual and Crosslingual Focused Evaluation. Proceedings of
    SemEval 2017.

### Adding Context
Added context to original dataset was done with OpenAI chatgpt-3.5, and cleaned by human annotators.
We use the following prompt:

`
Please provide a context to the given phrase, insert it into a long sentence, place it as part of the larger sentence and use the phrase verbatim. The sentence should also start with the letter <letter> the phrase is: <phrase>"}`


Where `<phrase>}` is replaced by the appropriate phrase from the dataset and `<letter>` is uniformly sampled from A-Z to increase diversity.

### Cleaning Data
We first automatically remove any example where the generated text does not have the original sentence verbatim (23%).<br>
We then let 2 human annotators validate the remaining examples removing cases where the generated text affects the similarity score (3%).

#### This dataset is used for a research paper currently under review. We ask that any usage of it awaits the publication of the paper and an appropriate open-source license that will be added at a later time.
