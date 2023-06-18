# Extracció atmosfèrica dels exoplanetes de la missió Ariel utilitzant mètodes de conjunt basats en arbres de decisió

Aquest repositori conté els notebooks creats com a part del meu Treball Final de Màster en Ciència de Dades a la [Universitat Oberta de Catalunya](https://www.uoc.edu) (Juny de 2023).

<figure>
<img align="left" src="https://imgur.com/i7yiUvA.jpg" width="350">
</figure>

En aquest treball s'ha investigat la viabilitat d'utilitzar models de conjunt basats en arbres de decisió per realitzar l'extracció atmosfèrica d'exoplanetes que s'analitzaran en la propera missió Ariel. Aquest estudi s'emmarca dins els esforços que s'estan fent actualment per trobar alternatives computacionalment més eficients a les tècniques tradicionals basades en inferència Bayesiana. Els resultats obtinguts demostren el potencial de les tècniques basades en Random Forest i Gradient Boosting per analitzar de forma eficient i fiable el gran volum de dades espectrals que s'espera obtenir en els propers anys. 

*Imatge adaptada d'[aquí](https://www.ariel-datachallenge.space/)*.


## Contingut

- **0 Preparar_dades.ipynb:** Preparació de les dades pel seu ús en la fase de modelització.

- **1 Exploracio_espectres.ipynb:** Anàlisi exploratòria dels espectres atmosfèrics

- **2 Exloracio_dades_auxiliars.ipynb:** Anàlisi exploratòria de les dades auxiliars

- **3 Random_forest_hiperparàmetres.ipynb:** Cerca en malla dels millors hiperparàmetres pel model Random Forest (RF).

- **4 Random_forest_train_i_resultats.ipynb:** Entrenament i avaluació de les prediccions pel model Random Forest (RF).

- **5 HistGB_hiperparams.ipynb:** Cerca en malla dels millors hiperparàmetres pel model Gradient Boosting basat en histogrames (HistGB).

- **6 HistBG_train_i_resultats.ipynb:** Entrenament i avaluació de les prediccions pel model Gradient Boosting basat en histogrames (HistGB).

- **7 XGBoost_hiperparams.ipynb:** Cerca en malla dels millors hiperparàmetres pel model XGBoost.

- **8 XGBoost_train_i_resultats.ipynb:** Entrenament i avaluació de les prediccions pel model XGBoost.

- **9 Comparacio_amb_nested_sampling.ipynb:** Comparació dels resultats obtinguts amb XGBoost, amb els obtinguts en una extracció atmosfèrica tradicional amb Nested Sampling.

## Requisits

Per executar els notebooks, cal prèviament descarregar les dades de l'ABC Database (Changeat i Yip, 2023), accessibles en [aquest repositori Zenodo](https://zenodo.org/record/6770103).

Aquestes dades es van publicar en el marc de l'[Ariel Data Challenge](https://www.ariel-datachallenge.space/), edició 2022.

## Resum del treball

En les darreres dues dècades s’ha descobert la presència de fins a 5272 exoplanetes, els quals ja han començat a redefinir la nostra comprensió sobre la formació i evolució dels sistemes planetaris. Actualment, s’estan centrant esforços en passar de la detecció a la caracterització d’aquests exoplanetes, és a dir, entendre de què estan fets. Gràcies a properes missions com el recent James Webb Space Telescope, i la missió Ariel de l’Agència Espacial Europea (prevista per llançament el 2029), s’espera obtenir una quantitat de dades espectrals sense precedents, les quals permetran caracteritzar la composició i propietats físiques de les atmosferes d’aquests mons llunyans.

Malgrat tot, els mètodes actuals per interpretar els espectres atmosfèrics són computacionalment molt costosos i poden representar un coll d’ampolla a l’hora de processar tot el volum de dades que es preveuen generar en els propers anys. Davant d’aquest escenari, l’àmbit de l'aprenentatge automàtic s’està plantejant com una alternativa potencialment més flexible i amb menys requeriments computacionals. Recentment s’ha posat a disposició de la comunitat científica l’Atmospheric Big Challenge Database (ABC Database) ([Changeat i Yip, 2023](https://arxiv.org/abs/2206.14633)), un conjunt de dades que simulen el volum i complexitat de dades que es mesuraran en la missió Ariel. Aprofitant l’oportunitat que representa aquest conjunt de dades, en aquest treball s'ha explorat l’ús de models de conjunt (Random Forest, Gradient Boosting) per tal d’extreure informació de temperatura i composició atmosfèrica a partir de dades espectrals.

Els resultats obtinguts han demostrat que aquesta família de tècniques, aplicades a l'ABC Database, tenen una capacitat de precció més elevada que el mètodes tradicionals d'inferència Bayesiana Nested Sampling. A més, tots els models desenvolupats han presentat uns temps d'entrenament de màxim 1.5 minuts, posant de relleu la seva eficiència computacional. En conseqüència, els mètodes de conjunt basats en arbres de decisió es posicionen com una alternativa prometedora als mètodes actuals per fer front al gran volum de dades que s'adquirirà en les properes missions dedicades a la caracterització atmosfèrica d'exoplanetes.

<br>

*In the last two decades up to 5272 exoplanets have been discovered, which have already begun to redefine our understanding of the formation and evolution of planetary systems. Recently, scientists have turned their attention from detection to the characterization of exoplanet atmospheres. Thanks to upcoming missions such as the recently launched James Webb Space Telescope, and the European Space Agency's Ariel Mission (due for launch in 2029), an unprecedented amount of atmospheric transmission spectra is to be obtained. These data will enable the characterization of the chemical composition and physical properties of these distant worlds.*

*However, current state-of-the-art methods for interpreting atmospheric spectral data are computationally expensive and may pose a bottleneck when processing the expected volume of data to be generated in the coming years. In this context, the field of machine learning is emerging as a promising alternative due to its high flexibility and rapid inference time. Recently, the Atmospheric Big Challenge Database (ABC Database, [Changeat and Yip, 2023](https://arxiv.org/abs/2206.14633)) has been released to the community. This data set simulates the quantity and quality of data that will be measured in the Ariel mission. Seizing the opportunity presented by this dataset, this study explores the use of ensemble models (Random Forest, Gradient Boosting) to retrieve temperature and chemical composition information from spectral data.*

*The obtained results have demonstrated that this family of techniques, applied to the ABC Database, exhibit higher predictive capabilities compared to traditional Bayesian method Nested Sampling. Furthermore, all developed models have shown training times of up to 1.5 minutes, highlighting their computational efficiency. Consequently, ensemble methods based on decision trees emerge as a promising alternative to current methods in handling the large volume of data expected to be acquired in future missions dedicated to the atmospheric characterization of exoplanets.*

## Referències

[Changeat and Yip, 2023](https://arxiv.org/abs/2206.14633). ESA-Ariel Data Challenge NeurIPS 2022: Introduction to exo-atmospheric studies and presentation of the Atmospheric Big Challenge (ABC) Database.
