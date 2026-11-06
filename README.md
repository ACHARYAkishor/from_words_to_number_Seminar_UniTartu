# From Words to Numbers: pseudo-quantification and the quantification of uncertainty

Teaching materials for a seminar of *Social Science Simulations* (SVUH.00.300), Institute of Social Studies, University of Tartu, autumn 2026.
Lecturer: ACHARYA Kishor.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ACHARYAkishor/from_words_to_number_Seminar_UniTartu/blob/main/Words_to_Numbers_UniTartu_ACHARYA.ipynb)

## What is here

| File | What it is |
|---|---|
| [`Words_to_Numbers_UT_ACHARYA.pdf`](Words_to_Numbers_UT_ACHARYA.pdf) | The seminar slides, 55 pages. GitHub shows the PDF in the browser; use the download button for a copy |
| [`Words_to_Numbers_UniTartu_ACHARYA.ipynb`](Words_to_Numbers_UniTartu_ACHARYA.ipynb) | The companion notebook: every experiment from the slides, with the code, sliders and the real data. Click the badge above to open it in Google Colab; nothing to install |
| [`wvs_estonia_justifiable.csv`](wvs_estonia_justifiable.csv) | The data the notebook uses: six published World Values Survey distributions for Estonia (avoiding a fare, cheating on taxes, accepting a bribe; 1996 and 2011), with a source link per row. **Required**: the notebook's first cell downloads it from here when it is not next to the notebook |
| [`wvs_estonia_README.txt`](wvs_estonia_README.txt) | Provenance and citation of the data file |
| `class_responses.csv` | Optional: the anonymous class questionnaire export. If it is absent, or has fewer than 15 rows, the notebook draws a synthetic class from the WVS distributions and says so in every title |
| [`questionnaire_form.txt`](questionnaire_form.txt) | The twelve questions of the class questionnaire, with the logic behind each |

The interactive version of the same six stops, with sliders and a short guide under each, is the **From words to numbers tour** on the course website: <https://acharyakishor.com/simulations>. The Monte Carlo tour there is the first half of the same story, and its materials are in [`Monte_carlo_Seminar_UniTartu`](https://github.com/ACHARYAkishor/Monte_carlo_Seminar_UniTartu).

## The seminar in one paragraph

Every number in a social simulation is a translation of something qualitative; every translation is a choice; and the choice must be written down as a distribution. The seminar follows one case, fare dodging on public transport treated as a social norm, through six stops: the gap between what a model needs and what research gives; turning an ordinal survey scale into a threshold by four defensible rules, and two ways to avoid needing a rule; turning text and expert judgement into distributions; separating four kinds of uncertainty (sampling, translation, heterogeneity, structural) and measuring which dominates; putting the distributions into Schelling's city and Granovetter's crowd with one line of code changed, where self-correction and a tipping point appear that a model of average citizens never shows; and what to report. The data are the World Values Survey's Estonian rounds of 1996 and 2011 and the class's own questionnaire.

No previous knowledge of Python, probability or statistics is assumed beyond the Monte Carlo seminar.

## How to use the notebook

1. Click the **Open in Colab** badge. Colab opens a copy in your own Google account; the original here is never changed.
2. Run the first (setup) cell. It loads the tools, fetches the data file from this repository, and shows a test slider; if you see the slider and the line "WVS data loaded: 6 distributions", everything works.
3. Work down the notebook. Each stop has a plain-words explanation, a code cell with line-by-line comments, a **▶ Try it** cell with sliders and a table of what to change and what to watch, and a box saying where the translation recipe is in that experiment.
4. To keep your changes, use *File → Save a copy in Drive* inside Colab.

If you run the notebook locally instead of in Colab, put `wvs_estonia_justifiable.csv` (and, if you have it, `class_responses.csv`) in the same folder; the setup cell looks there first. If the sliders do not appear, install a recent `ipywidgets` (`pip install -U ipywidgets`) and restart the kernel. Every Try it cell also works without sliders: change the number in its first line and run it again.

## Data

World Values Survey, Estonia, wave 3 (1996, n = 1,021) and wave 6 (2011, n = 1,533), items "justifiable: avoiding a fare on public transport / cheating on taxes / accepting a bribe" (variables V193, V194, V196 and V199, V201, V202). Counts of valid cases, unweighted, read from the survey documentation in the IHSN catalogue ([1996](https://catalog.ihsn.org/catalog/9087), [2011](https://catalog.ihsn.org/catalog/9049)); the same figures are available from the [WVS online analysis tool](https://www.worldvaluessurvey.org/WVSOnline.jsp).

Cite as: Inglehart, R., Haerpfer, C., Moreno, A., Welzel, C., Kizilova, K., Diez-Medrano, J., Lagos, M., Norris, P., Ponarin, E. & Puranen, B. (eds.) (2014). *World Values Survey: Round Three (1995–1998) and Round Six (2010–2014), Country-Pooled Datafiles.* Madrid: JD Systems Institute.

The class questionnaire is anonymous; no names or e-mail addresses were collected.

## Licence

Slides, text and figures: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code in the notebook: MIT. Please credit *ACHARYA Kishor, University of Tartu* when reusing.

## References

- Bicchieri, C. (2017). *Norms in the Wild: How to Diagnose, Measure, and Change Social Norms.* Oxford University Press.
- Clark, W. A. V. (1991). Residential preferences and neighborhood racial segregation: A test of the Schelling segregation model. *Demography*, 28(1), 1–19.
- Farley, R., Schuman, H., Bianchi, S., Colasanto, D., & Hatchett, S. (1978). "Chocolate city, vanilla suburbs": Will the trend toward racially separate communities continue? *Social Science Research*, 7(4), 319–344.
- Granovetter, M. (1978). Threshold models of collective behavior. *American Journal of Sociology*, 83(6), 1420–1443.
- Inglehart, R. et al. (eds.) (2014). *World Values Survey: Round Three and Round Six, Country-Pooled Datafiles.* Madrid: JD Systems Institute.
- Lazarsfeld, P. F. (1958). Evidence and inference in social research. *Daedalus*, 87(4), 99–130.
- O'Hagan, A., Buck, C. E., Daneshkhah, A., Eiser, J. R., Garthwaite, P. H., Jenkinson, D. J., Oakley, J. E., & Rakow, T. (2006). *Uncertain Judgements: Eliciting Experts' Probabilities.* Wiley.
- Schelling, T. C. (1971). Dynamic models of segregation. *Journal of Mathematical Sociology*, 1(2), 143–186.
- Stevens, S. S. (1946). On the theory of scales of measurement. *Science*, 103(2684), 677–680.
