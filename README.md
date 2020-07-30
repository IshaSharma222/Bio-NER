# Bio-NER
Research project on gene name extraction using NER to detect relationship between DNA methylation and neurogenerative diseases and also study novel coronavirus disease
## Project Summary
# Title- Research Project on gene name extraction
# Goal- Use NLP to detect the relationship between DNA methylation and neurodegenerative diseases and also study the causes and risk factors of COVID-19
Individual Progress:
 Overview -
1. Read two research papers- Ohta T, Pyysalo S, Miwa M, Tsujii J. Event
extraction for DNA methylation. J Biomed Semantics. 2011;2 Suppl 5(Suppl
5): S2. Published 2011 Oct 6. doi:10.1186/2041-1480-2-S5-S2; Fang, Y., Lai,
P., Dai, H. et al. MeInfoText 2.0: gene methylation and cancer relation
extraction from biomedical literature. BMC Bioinformatics 12, 471 (2011).
https://doi.org/10.1186/1471-2105-12-471

2. Collected around 820 PubMed articles related to genes/proteins, DNA
methylation and neurodegenerative diseases using annotated articles present
in PubTator Central.

3. Performed Bio-NER on a sample from this data using ‘en_ner_craft_md’ - a
spaCy NER model trained on CRAFT corpus. The Colorado Richly Annotated
Full-Text (CRAFT) Corpus is a collection of 97 full-length, open-access
biomedical journal articles that have been annotated both semantically and
syntactically to serve as a research resource for the biomedical
natural-language-processing (NLP) community. I chose CRAFT as it
identifies all mentions of nearly all concepts from nine prominent biomedical
ontologies and terminologies: the Cell Type Ontology, the Chemical Entities of
Biological Interest ontology, the NCBI Taxonomy, the Protein Ontology, the
Sequence Ontology, the entries of the Entrez Gene database, and the three
sub ontologies of the Gene Ontology.

4. Built a knowledge graph In order to extract the genetic information,
methylation and pathway information for the diseases. The relationship of SO
in the context of the given text could also be extracted using this.

5. The knowledge graph was built using spacy. Firstly various NLP techniques
were performed i.e. sentence segmentation, dependency parsing, parts of
speech tagging, and entity recognition to convert it into a machine-readable
format.

6. Then I wrote a get-relation function that tries to find the ROOT word or
main-word in a sentence. Once the ROOT is identified, then the pattern
checks whether it is followed by a preposition (‘prep’) or an agent word. If yes,
then it is added to the ROOT word. This helps to find the predicates or relation
between entities.

7. Finally, a knowledge graph was created from the extracted entities
(subject-object pairs) and the predicates (relation between entities).

8. Read another research paper to improve knowledge graphs: Relation Prediction of Co-morbid Diseases Using Knowledge Graph Completion by Saikat Biswas, Pabitra Mitra, and Krothapalli Sreenivasa Rao(can be found under research papers folder).

9. The skills gained from this project are now being applied to study the causes and risk factors of COVID-19.

10. Kaggle kernels containing the knowledge graph code can be found here: 
  https://www.kaggle.com/isha20/covid-knowledge-graph
  https://www.kaggle.com/isha20/covid-19-knowledge-graph
