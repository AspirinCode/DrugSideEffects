### about these files
As the code currently stands it is now generic enough to tackle any disease as long as the users know the UMLS code for their disease of interest e.g. "C0002395" is the code for Alzheimer's disease.

`reviewers_JBI_LoadData.R` - as it suggests loads in the tsv. files and creates the R data structures.

`reviewers_JBI_DrugList.R` - performs (so far) the majority of the processing to generate the candidates drugs for repurposing.

`reviewersJBIloadData.RData` - is the R environment from reviewers_JBI_LoadData.R avoids the need to run it everytime you power up R.

`venn-5.pdf` - example Venn Diagram for Alzheimer's drugs and their common overlapping side-effects. The diagram is limited to five groups (drugs) maximum and so the central value of 10 is in fact 8, because 9 drugs were used to generate the candidate drugs. Just be aware of this limitation when plotting Venn's if you have more than five drugs. Generally, the more drugs you conduct the search with, then the fewer side-effects these will have in common.

### Whats next?
I need to write a number functions to handle:

1. Direct R communications with STITCH database - so far I manually create protein interactions using their browser.

2. Pathway analysis with KEGG or Reactome - I have used hard coded solutions so far (for Alzheimers') and need to make it generic for any disease with functions.

3. Perhaps trickest of all will be to tackle the issues of relating a given side-effect to the biochemical pathways involved.

4. Integrate the various the sources of the disparate data in a coherent way. So far the system has been a series of isolated analyses, each important in its own right but lacking an overarching synthesis. The usual way in the literature is to generate a 'fingerprint' that integrates the presence or absence of a parameter using '1s' or '0s', a method that typically generates huge arrays.

5. Comparison with existing methods - might be tricky as not all the software is freely available.
