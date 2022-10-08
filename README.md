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
  
<h3 align="left">Environmental Data:</h3>
  
```mermaid
flowchart LR
id1[(Working Directory)] --> |Environmental Metadata| B(read.csv)
B --> |Data Cleaning &</br>Subsetting| C(tidyverse)
C --> |Get Summary of </br>Inferential Stats| D(summarySE)
C--> |Do a Quick Plot| E(qplot)
C --> F(glm)
F-. Normality Test .->G(shapiro.test)
F--> |Homoscedasticity| H(bptest)
subgraph F
direction TB
F--> |Interactions of Factors| I(TukeyHSD)
end

```
