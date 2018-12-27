# docsearch
A python-based search engine for a relatively small corpus of documents.

The overall idea is to build a search engine where the search targets form a relatively small, fixed corpus of documents. 

Initially document clustering is carried out on the corpus and a hierarchy is built where the "leaves" of the hierarchy are individual documents. The clustering results in terms associated with clusters at every level. 

As the search engine is used, extra terms are recorded and associated with the final document selected by the user.

Overall, the search mechanism is interactive with usually several input steps from the engine and several from the user. Initially the user enters the search phrase. The search engine identifies the cluster(s) at various levels which seem to match the search best, It then works out which distinguishing terms would best identify the sub-clusters and sub-sub-clusters etc. corresponding to the user's search. The user is then presented with a set of terms and asked to select the ones which most appropriately match their search. The terms offered by the engine are a combination of those which will narrow the search and some which confirm that the best clusters have not been inadvertently omitted.

So, this search engine does some "learning" because it fits new terms originating from the user into the indexing which can speed up future searches.