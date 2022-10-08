# Practice | Mermaid-Markdown
 
<h3 align="left">Objective:</h3>
  To practice creating a simple flowchart for each of my research method
  
<h3 align="left">References:</h3>
  https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/
  https://tuts.alexmercedcoder.dev/2022/2/why-all-developers-should-master-markdown/
  https://mermaid-js.github.io/mermaid/#/n00b-syntaxReference
  
<h3 align="left">Note:</h3>
  Codes are case sensitive,avoid spaces and read syntax
  
  ```mermaid
  graph TD;
  Raw_Data-->Backup_Data;
  Raw_Data-->Process_Data;
  Process_Data-->Clean_Data;
  Clean_Data-->R;
  R-->Statistical_Analyses;
  Statistical_Analyses-->Data_visualizations;
  ```
  
<h3 align="left">Physicochemical & Physiological Data:</h3>
  
```mermaid
flowchart LR
id1[(Working Directory)] --> |Environmental Metadata| B(read.csv)
B --> |Data Cleaning &</br>Subsetting| C(tidyverse)
C --> |Get Summary of </br>Inferential Stats| D(summarySE)
C--> |Do a Quick Plot| E(qplot)
C --> F(glm)
F-. Normality Test .->G(shapiro.test)
F--> |Homoscedasticity| H(bptest)
subgraph Interactions
direction TB
F--> I(TukeyHSD)
end

```

<h3 align="left">CCA Data:</h3>

```mermaid
flowchart LR
id1[(Working Directory)] --> |CCA Metadata| B(read.delim)
B --> |Data Cleaning,</br>Subsetting, &</br>Transposition| C(tidyverse)
C --> |Create CCA Model| D(cca)
C--> |Get summary of CCA Model| E(summary)
C --> |Apply VIF less than 10|F(ordistep & vif.cca)
F-. Global Test .->G(anova.cca)

```
