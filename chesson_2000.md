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
- We can extend to multispecies communities with diffuse competition via the following rough model: \begin{equation} \bar{r}_i \approx b_i (k_i - \bar{k}) + \frac{b_i (1 - \rho) D}{n - 1} \end{equation} with $$n$$ the total number of species, $$k$$s as fitnesses, $$\bar{k}$$ as th average fitness of $$i$$'s competitors, $$\rho$$ as niche overlap, and $$D$$ a positive constant
  - If the stabilizing (second) term is greater in magnitude than the relative average fitness for the worst species, all species coexist  
- Two types of mechanisms can increase coexistence
  - Decrease the fitness difference (first term), i.e., **equalizing mechanisms** 
  - Increase the stabilzing term, i.e., **stabilizing mechanisms** 
- How do stabilizing mechanisms arise?
  - First, consider four "dimensions" of niche space: recourses, predators, time, and space 
  - A niche is defined by the effect and response a species has at each point in niche space
  - An example of a stabilizing mechanism is density dependence
    - Species $$a$$ depends on a resource (has a strong response at a point in niche space) and reduces the resource (has a strong effect)  
    - Species $$b$$ has a similar relationship to a resource as species $$a$$, but with a different resource
    - Even if there is a bit of resource overlap, intraspecific competition will be stronger than interspecific competition, resulting in stable coexistence
    - However, under certain assumptions -- for example, if one resource is much richer than another, introducing a non-zero fitness difference -- stable coexistence is not guaranteed
    - Another assumption is that resources have independent dynamic

## Fluctation-dependent and fluctuation-independent mechanisms
- Stable coexistence mechanisms can be fluctuation independent
  - e.g., resource partitioning, frequency-dependent predation
  - Often modelled by deterministic equations with stable equilibrium points
  - The mechanisms largely operates independently of fluctuations in the system
- Some coexistence mechanisms depend on fluctuations, i.e., are **fluctuation dependent**
  - We can divide these mechanisms into two classes: *relative nonlinearity of competition* and *the storage effect* 

### Relative nonlinearity of competition
- Per capita growth rate is often a nonlinear function of limiting factors
- For a single limiting factor, the per capita growth rate can be expressed as \begin{equation} r_i(t) = E_i(t) - \phi_i(F) \end{equation} with $$E_i(t)$$ the maximum per capita growth rate as a function of environmental conditions (which may fluctuate), $$F$$ as the limiting factor, and $$\phi_i(F)$$ as the response defining dependence of per capita growth rate on $$F$$
  - We can express the degree of nonlinearity with some quantity $$\tau$$
  - If two species have different values of $$\tau$$, for coexistence to occur, the species with a larger value must:
    - Have a mean fitness advantage in the absence of fluctuations
    - Experience lower fluctuations when it is an invader than a resident 
- Consider the following approximation to $$\bar{r}_i$$ for a species $$i$$ in the presence of a competitor $$s$$: \begin{equation} \bar{r}_i = b_i(k_i - k_s) - b_i(\tau_i - \tau_s) V(F^{-i}) \end{equation} whre the first term is the fitness difference term in the absence of fluctuations, $$\tau_i - \tau_s$$ is the difference in nonlinearities, and $$V(F^{-i})$$ is the variance of the limiting factor of invader $$i$$ and resident $$s$$
  - The second term changes sign when invader and resident are switched
  - The species with a more positive nonlinearity is disadvantaged by fluctuations
  - Let $$B$$ be the average of $$V(F^{-i})$$ for each species as invader and let $$A = \frac{1}{2} \mid V(F^{-i})_1 - V(F^{-i})_2 \mid$$; then if the species with smaller nonlinearity ($$\tau$$) experiences larger $$V(F)$$ as an invader, we have \begin{equation} \bar{r}_i \approx [b_i(k_i - k_s) - b_i(\tau_i - \tau_s) B] + b_i \mid \tau_i - \tau_s \mid A \end{equation}.
    - The first term is the equalizing term, and the second is the stabilizing term
    - Nonlinearity can thus be both stabilizing and equalizing
      - But the "stabilizing" term might actually be destabilizing because the term can be negative  

### The storage effect
- Environmental fluctuation may reduce population density and reduce competition, but this does not imply coexistence
- Stable coexistence rsults from environmental fluctuation due to temporal niches: species use resources at different times
- The storage effect is the outcome of temporal niches resulting in greater intraspecific than interspecific competition
  - Three important ingredients:     
  (1) Differential responses to the (varying) environment  
  (2) Covariance between environment and competition -- i.e., covariance between effects of environment on per capita growth rat of a population (environmental response) and of competition on the growth rate (competitive response) -- so that when a species is favored by the environment, it experiences intraspecific competition, and vice versa  
  (3) Buffered population growth, which limits the impact of competition when a species is not favored by the environment, e.g., dormancy at unfavorable times of the year
- Models including the storage effect can give approximate long-term low-density growth rates like: \begin{equation} \bar{r}_i \approx b_i(k_i - \bar{k}) + \frac{b_i (1 - \rho) (-\gamma) \sigma^2}{n - 1}  \end{equation} where $$-\gamma$$ measures buffered population growth, $$\sigma^2$$ is the variance in environmental response, and $$\rho$$ is the correlation between envrionmental responses of different species

### Mechanisms in combination integrated over temporal scales
- Competition and the physical environent drivethe aforementioned mechanisms affecting coexistence
- The long-term low-density growth rate can also be expressed as: \begin{equation} \bar{r}_i \approx \bar{r}^{'}_i - \Delta N + \Delta I, \end{equation} with $$\Delta N$$ the relative nonnlinearity of competition and $$\Delta I$$ the storage effect

## The spatial dimension
- Spatial variation is generally similar to temporal variation re: coexistence
- Differential responses to the environment are usually met in spatially variable models in two ways:
  - Relative fitnesses of different species vary in space
  - Relative variation in dipersal into different habitats
    - Gives rise to covariance between environment and competition  
- Buffered population growth is automatic in spatially variable habitats, though strength is variable
- Tilman's resource ratio hypothesis: the ratio of the rates of supply of two limiting rsources at a locality determines a unique pair of plant species from a given regional pool able to coexist there
  - Supply rate varies spatially, so different pairs coexist at different placs
- There are two general kinds of competition-colonization tradeoffs:
  - A patch supports a local community that is destroyed by random disturbance and recolonized by other patches
  - A patch supports a single organism whose death opens the patch for recolonization
  - For coexistence to occur, colonizing ability should be inverse to competitive ability  

## Predators, herbivores, and pathogens



