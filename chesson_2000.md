# Mechanisms of maintenance of species diversity

- What is diversity maintenance? "coexistence in the same spatial region of species having similar ecology," including overlapping resource requirments
  - Alternatively, to general maintenance of species richness and evenness, but not the focus here 
  - The area under study should be large enough such that pop. dynamics are not greatly affected by migration  

## Stable Coexistence

- Stable coexistence means densities of species show no long-term trends (i.e., if densities are low, species generally recover)
- Unstable coexistence means species may not recover and may die out
- We can express stable coexistence in rough quantiativ terms using the invasiability critierion (i.e., that each species can increase from low density in the presence of the rest of the community
  - Species must have positive long-term low-density growth rates, $$\bar{r}_i$$ 
  - What is necssary for $$\bar{r}_i > 0$$?
    - Species must be distinguished in ecologically significant ways -- but what is ecologically significant? 
- Consider Lotka-Volterra compeition: \begin{equation} \frac{1}{N_i} \cdot \frac{d N_i}{dt} = r_i (1 - \alpha_{ii} N_i - \alpha_{i j} N_j), \ \ \ i = 1, 2, \ j \neq i. \end{equation} with $$\alpha_{ii}$$ the intraspecific competition coefficient and $$\alpha_{ij}$$ the interspecific competition coefficient
  - If $$\alpha_{jj} > \alpha_{ij}$$, then $$i$$ can persist in the presence of $$j$$, i.e., $$j$$ cannot exlude $$i$$ if the effect $$j$$ has on itself is greater than the effect $$j$$ has on $$i$$
  - It is easy to extend Lotka-Volterra models to have nonlinear per capita growth rates: simply set $$\alpha_{ij} = f_{ij}(N_i, N_j)$$
- Lotka-Volterra models and extensions can be thought of as models of direct competition or as descriptions of dynamics arising from resource dynamics
- An example of explicit resource competition is Tilman's theory (the $$R^{*}$$ rule):
  - For species jointly limited by a resource, the winner of compeitition has the lowest $$R^{*}$$, which is the lowest level of a resource required for the species' persistence
  - $$R^{*}$$ is influenced by many factors (basically, overall fitness)
 - Now consider a simple resource limitation model: \begin{equation} \bar{r}_i = b_i \left( \frac{\mu_i}{b_i} - \frac{\mu_s}{b_s} \right) \end{equation} where $$\mu$$ is a man per capita growth rate in the absence of resource limitation and $$b$$ is the rate at which the per capita growth rate decreases with resource limitation
  - $$\mu/b$$ measures the average fitness of the species; $$\max{\mu/b}$$ gives the winner of competition
  - But even in the presence of tradeoffs, which may draw fitnesses closer together, one species is necessarily going to win and coexistence is not possible 
 - Consider, alternatively, MacArthur's derivation of Lotka-Volterra competition: \begin{equation} \bar{r}_i = \frac{1}{N_i} \cdot \frac{d N_i}{dt} = b_i (k_i - k_s) + b_i(1 - \rho) k_s  \end{equation} where $$k$$ is equivalent to $$\mu/b$$ from the previous model, and $$\rho$$ measures resource-use overlap
  - The first term is the average fitness comparison from the previous model
  - The second term is a stabilizing term
  - **Species coexist if the stabilizing term is greater than the fitness difference**
  - The stabilizing term arises from a tradeoff in resource use 
- We can extend to multispecies communities with diffuse competition via the following rough model: \begin{equation} \bar{r}_i \approx b_i (k_i - \bar{k}) + \frac{b_i (1 - \rho) D}{n - 1} \end{equation} with $$n$$ the total number of species, $$k$$s as fitnesses, $$\bar{k}$$ as th average fitness of $$i$$'s competitors, $$rho$$ as niche overlap, and $$D$$ a positive constant
  - If the stabilizing (second) term is greater in magnitude than the relative average fitness for the worst species, all species coexist 
