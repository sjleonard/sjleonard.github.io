
[Home](index.md)

# Table of Contents
1. [Chapter 1](#1)
    1. [Historical overview](#1.1)
    2. [A bit of natural history](#1.2)
    3. [Coevolution in multispecific mutualisms](#1.3)
2. [Chapter 2](#2)
    1. [A network approach to complex systems](#2.1)
    2. [Measures of network structure](#2.2)
    3. [Models of network buildup](#2.3)
    4. [Ecological networks](#2.4)


# Chapter 1. Biodiversity and Plant-Animal Coevolution <a name="1"></a>

## Historical overview <a name="1.1"></a>

- People have been studying plant-animal mutualisms since the mid 19th century
  - Darwin was interested in plant-animal interactions, even predicted secondary extinctions
- de Bary (1879) coined the term *symbiosis*
- But antagonistic interactions like predation and competition (emphasized by e.g., Clements and Tansley) were more central in ecology 
  - Also in Lotka-Volterra models, even though Gause and Witt (1935) proposed similar mutualistic models
- Reasons why mutualisms may not have been more widely studied:
  - Difficult to find stable solutions to dynamic models of mutualism
  - Lack of empirical tools and theory made synthesis difficult
  - Stigmatized due to association with anarchism
- Ehrlich and Raven's (1964) paper on coevolution reignited interest
- Mutualisms are old and very functionally important
  - Pollination is at least 200 million years old, common by 100 m.y.a.
  - Pollination and seed dispersal are critical for the functioning of ecosystems
    - But are threatened by anthropogenic pressures like hunting and habitat loss
    - Large seed dispersers are going extinct at an especially high rate
    - In the geological record, insect extinction or decline is often followed by extinction of flowering plants
- Study of mutualistic interactions has shifted from early focus on one-to-one interactions to greater incorporation of community context
  - Recent recognition that generalism is widespread (Chittka et al., 1996)

## A bit of natural history <a name="1.2"></a>

- Mutualisms are among the mst common interactions in terrestrial communities (Janzen, 1985)
- Major groups of mutualistic interactions (though focus of this book is first two):
    - Pollination
    - Seed dispersal among animals and plants
    - Protective mutualisms among ants and plants
    - Harvest mutualisms
    - Humans and other organisms (e.g., agriculture, husbandry)
- Most mutualisms likely lie somewhere on gradient of effectiveness from antagonism towards legitimate mutualism
- Seed dispersal is not a harvest mutualism because fitness of mother also increases as a result of mutualism
- An efficient disperser (1) efficiently consumes seeds and (2) spreads seeds far from mother plant (where successful germination and establishment is more likely)
    - Especially with frugivory, though, there is usually seasonality, so frugivores need diversified diets
        - Plant-frugivore mutalisms typicaly show low specificity (Jordano, 1987)  
- Alternatively, pollination tends to benefit from high specificity of interactions
    - Pollen should be carried to conspecific flowers
    - Pollinators don't necessarily need as diverse diets
    - Flowers also tend to signal receptivity to pollination (e.g., by color and odor) more than plants with seeds

## Coevolution in multispecific mutualisms <a name="1.3"></a>

- Coevolution involves joint evolutionary trajectories of separate gene pools that do not mix
- Coevolution is one of the results of plant-animal mutualisms
- Most multispecific interactions are diversified, but it's hard to predict the effects of coevolution on a network of hundreds of interacting species - "diffuse coevolution"
- However, a big advance has been John Thompson's idea of "geographic mosaics of coevolution"
    - Most mutualisms have both spatial and temporal variability and seem context-dependent
    - Thompson's idea has three main premises  
    (1) Interactions occur among species distributed in populations  
    (2) Outcomes of interactions vary across populations  
    (3) Interacting species do not necessarily have matching geographic ranges  
    - These premises produce predictions:  
    (1) There is mosaic of selection across populations, leading to different evolutionary trajectories  
    (2) There may only be coevolution occurring in some populations (coevolutionary hotspots)  
    (3) There will be remixing of traits due to gene flow, drift, and local extinctions  
- The next step is to extend from multispecific systems to whole networks, which is what this book is about
    - To do this, we need network theory  


# Chapter 2. An Introduction to Complex Networks <a name="2"></a>

## A network approach to complex systems <a name="2.1"></a>

- A network (or graph) is a set of vertices (or nodes) connected by edges (or links), i.e., a pair $$(G,V)$$
    - A graph is a mathematical object, but can be used in science to represent relationships between objects
        - e.g., genes linked by gene regulation, proteins interacting to create structure, species in a food web, etc.  
- Erdos and Renyi began studying random graphs
    - An Erdos-Renyi graph describes a collection of vertices in which each two vertices have probability $$p$$ of being connected
    - The size of the largest average cluster in an Erdos-Renyi graph increases nonlinearly in $$p$$, with a critical point $$p_c$$
    - Random graphs can be useful as null models and rarely represent reality well
    - The number of edges per vertex in such a graph follows a Poisson distribution 
        - Reminder: the probability mass function of a Poisson distribution is: $$\text{Poisson}(\lambda) = \frac{\lambda^k e^{- \lambda}}{k!}$$

**One-mode and two-mode networks**

- In one-mode networks (e.g., food webs), there is only one type of vertex (e.g., servers), and any two vertices can be connected
- In two-mode networks (e.g., mutualistic networks), a.k.a. bipartite graphs, there are two types of vertices, and edges can only exist between different types of vertices
    - A bipartite graph can be represented as an adjacency matrix $$X$$, where $$X_{i, j} = 1$$ if vertex $$i$$ of class $$A$$ and vertex $$j$$ of class $$B$$ are connected, and $$X_{i, j} = 0$$ otherwise
    - The unipartite graph has a similar representation but without classes like $$A$$ and $$B$$
    - Graphs can also be weighted, where $$X_{i, j}$$ can take on values beyond $$0$$ and $$1$$

## Measures of network structure <a name="2.2"></a>

**Connectivity distribution**

- The *degree* of a vertex is the number of edges connected to that vertex
- The *degree distribution* describes the distribution of degrees of vertices in a graph
    - It is a probability mass function; common to also represent the degree distribution with a cdf (cumulative distribution function) 
    - Random graphs often have relatively homogeneous degree distributions
    - Often plotted on a log-log scale
        - Random graphs show exponential decay on this scale
- Approximate *scale-free* distributions are relatively common in real-world networks
    - In such network, most vertices have few links but a few vertices have a lot of links
    - Scale-free networks are described by a power-law distribution, $$P(k) \propto k^{- \gamma}$$, which gives the probability of a vertex having $$k$$ edges, with $$\gamma$$ a critical exponent
    - Linear on a log-log scale (with slope $$- \gamma$$)
    - High-degree vertices in real-world networks are important for understanding robustness
         - Networks are robust to disturbance of most (low-degree) nodes but susceptible to disturbance of high-degree nodes
         - Robust to random disturbances, but potentially susceptible to targeted ones

- In addition to scale-free networks, truncated scale-free networks and single-scale networks are also common
- There are a couple common type of scale-free ecological patterns
    1. Bivariate relationships between e.g., species-area, body-size allometries
    2. In which frequency is related to magnitude (e.g., number of interactions per species)

**Strength distribution**

- We can move beyond binary networks and quantify the strength of interactions (or something else, like flows) via edge weights
- The *strength* of a vertex is the sum of its edge weights 
- As with a degree distribution, we can plot the strength distribution

**Small-world networks**

- Stanley Milgram showed in 1967 that the average distance between two individuals is only around six degrees, ranging from two to ten
- Many real-world networks are scale-free and/or small-world networks
- Watts and Strogatz (1998) formalized the idea of small-world networks:
    - High clustering coefficient
    - Short path length 
- Some studies have shown small-world networks in ecology, e.g. in food webs (Montoya and Sole, 2002) and pollination networks (Olesen, Bascompte, et al., 2006), but the generality of this has also been disputed
    - Dunne et al. (2002) argue that most ecological networks are not highly clustered, though they do often have short path lengths   

**Modularity**

- In modular networks, there exist highly-connected modules of vertices (aka communities, compartments, or cliques, though cliques also technicallyr refer to *completely* connected groups of vertices), but vertices from different modules are only weakly connected
- Modularity is an important component in understanding the functioning of complex networks, including ecological networks
- Quantifying modularity (roughly equivalent to community detection) is not necessarily straightforward, but there are algorithms to do it (e.g., simulated annealing)
- For bipartite networks, the modularity function is \begin{equation}
M = \sum_{i = 1}^n \left( \frac{e_i}{L} - \frac{d_i^P}{L} \frac{d_i^A}{L} \right),
\end{equation}
with $$n$$ the number of modules, $$e_i$$ the number of observed interactions within module $$i$$, $$L$$ the total number of interactions in the network, and $$d_i^P$$ and $$d_i^A$$ the sums of the degrees of nodes in module $$i$$ for the plant ($$P$$) and animal ($$A$$) sets

- In food webs, phylogeny, body size, and habitat preference seem to be significantly correlated to a species' ascription to a module, but modularity has not been studied much overall
- Modularity techniques have begun to be applied to mutualistic networks (Olesen, Bascompte, et al., 2007)

**Motifs and subgraphs**

- Motifs are repeated subgraphs, overrepresented in complex networks compared to random graphs
- The idea sort of originated in social network analysis as *triads*, particular three-node subgraphs
- Introduced to ecology by Bascompte and Melian (2005) to study important subgraphs in food webs
    - Competition and intraguild predation are overrepresented, but frequency of omnivory varies 
- The functional consequences of certain motifs was not studied until recently
    - Stouffer and Bascompte (2010) showed that the most common modules in food webs are those that confer the most robustness/persistence
    - The processes that give rise to overrepresentation of certain motifs is still unclear

## Models of network buildup <a name="2.3"></a>

- The first model of network formation is the random graph formation of Erdos and Renyi
- A second major model of network formation was that of Watts and Strogatz (1998), who modeled small-world networks
    1. Begin with a regular lattice, where each vertex is connected to two nearest neighbors
    2. Rewire two distant nodes with probability $$p$$
        - As $$p$$ increases, the model becomes closer to an Erdos-Renyi graph
- Barabasi and Albert (1999) sought to model formation of scale-free networks via *preferential attachment*; their "rich-get-richer" process produces many vertices with few connection and a few vertices with many connections, as in scale-free networks
    1. Begin with an Erdos-Renyi graph
    2. Add a new vertex
    3. The probability that the new vertex is connected to an existing vertex is proportional to the degree of the existing vertex
    4. Repeat 

## Ecological networks <a name="2.4"></a>

- Networks have been used in ecology as far back as the 1950s; here we review some other uses
    - Two main types: spatial networks (with vertices representing habitat patches) and species-level interaction networks (e.g., food webs, epidemiological networks)

**Spatial networks**

- Especially due to anthropgenically driven habitat fragmentation, metapopulation theory is currently a very important topic of research in ecology
    - Originated with Levins (1969), who studied a (theoretical) system of infinite equal patches and dynamical balance between extinction and recolonization
    - Research eventually moved to spatially explicit models, with Urban and Keitt (2001) using graph theory to think about spatial metapopulations
        - Spurred similar research on riverine newtorks, patches of ponds with amphibians, gene flow, etc.

**Food webs**

- Food webs have been around sinc at least Camerano (1880) and Pierce et al. (1912), who were both interested in how different food web interactions can be positive or negative for humans
- Modern food web analysis probably began with Lindeman (1942) and Odum (1956)
- Earlier food web models (from a few decades ago and later), were focused on global descriptors like connctance, compartments, fraction of top predators, and invariance
- Paine (1969, 1992) helped show the importance of top predators (as keystone species) and described the role of interaction strength
- Robert May studied stability and complexity in model ecosystems using food webs (1972), inspiring a lot of further research
    - He showed that in random food webs, greater diversity promotes lower stability
    - May's finding ran counter to many (field) ecologists' intuitions; real food webs must be non-randomly assembled in such a way as to (probably) promote stability
    - May suggested modularity might promote stability, but Pimm (1979) argued that compartments would make food webs less stable
- Another area of theoretical research works on models of network buildup for food webs, based on simple ideas
    - e.g., larger animals eat smaller ones
    - Can incorporate niche information (Williams and Martinez, 2000), phylogenetic info (Cattin, Bersier, et al., 2004)
      
**Host-parasitoid networks**

- Parasitoids are predatory arthropods that lay eggs inside, on top, or near hosts, with the host later used as food by larvae; very common in nature
- Relatively simple interaction, amenable to modeling and theory
- Though these are technically food-web interactions, they are also often represented as two-mode networks
- Host-parasitoid interactions are antagonistic, thus host-parasitoid networks are expected to look different than mutualistic networks
    - Mutualistic networks may facilitate incorporation of new species; antogonistic networks may favor escalating arms races and compartmentalization  

**Epidemiological networks**


