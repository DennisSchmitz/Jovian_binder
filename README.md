# Jovian_binder, a public demo report of the [Jovian viromics pipeline](https://github.com/DennisSchmitz/Jovian) rendered by [Binder](https://mybinder.org/)

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DennisSchmitz/Jovian_binder/master?filepath=Notebook_report.ipynb)

## Update checklist

Every update the following must done to downsize data and redact server information:  

- From the MultiQC report, remove the '<div id=analysis_dirs_wrapper>` block from the HTML.
- The Krona and MultiQC raw data folders are not necessary, only the HTML is required.
- Downsize the scaffold tables via `head -1000 [INPUT_FILE] | awk 'BEGIN {FS="\t"; OFS="\t"}; NF{NF-=1};1' > [OUTPUT_FILE]`. It limits it to 1000 rows and removes the last column containing the sequences.
- Downsize the virushost and SNP tables to 500 rows via `head -500 [INPUT_FILE] > [OUTPUT_FILE]`.
- Do not upload the log_index or child-logs.
- Redact the pathing from `data/log_conda.txt`.
- Do not upload the log_database file.

#### Authors
- Dennis Schmitz ([RIVM](https://www.rivm.nl/en) and [EMC](https://www6.erasmusmc.nl/viroscience/))  
- Sam Nooij ([RIVM](https://www.rivm.nl/en) and [EMC](https://www6.erasmusmc.nl/viroscience/))  
- Robert Verhagen ([RIVM](https://www.rivm.nl/en))  
- Thierry Janssens ([RIVM](https://www.rivm.nl/en))  
- Jeroen Cremer ([RIVM](https://www.rivm.nl/en))  
- Florian Zwagemaker ([RIVM](https://www.rivm.nl/en))  
- Mark Kroon ([RIVM](https://www.rivm.nl/en))  
- Erwin van Wieringen ([RIVM](https://www.rivm.nl/en))  
- Harry Vennema ([RIVM](https://www.rivm.nl/en))  
- Annelies Kroneman ([RIVM](https://www.rivm.nl/en))  
- Marion Koopmans ([EMC](https://www6.erasmusmc.nl/viroscience/))  

____
_This project/research has received funding from the European Union’s Horizon 2020 research and innovation programme under grant agreement No. 643476._
____
