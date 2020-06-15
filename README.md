<p align="center"><img src="https://github.com/LINCnil/GDPR-Developer-Guide/raw/master/templates/BANNIERE-EN.JPG" width="100%" align="middle"></p>


# GDPR Guida per sviluppatori

#### Al fine di aiutare gli sviluppatori di applicativi e di siti web a rendere il loro lavoro rispondente ai requisiti del GDPR, lo CNIL ha redatto una nuova guida alle buone pratiche sotto licenza aperta, in modo che possa essere arricchita da altri professionisti.

Questa guida è pubblicata con [licenza GPLv3](https://www.gnu.org/licenses/gpl-3.0.html) e [open license 2.0](https://www.etalab.gouv.fr/wp-content/uploads/2017/04/ETALAB-Licence-Ouverte-v2.0.pdf) (esplicitamente compatibile con [CC-BY 4.0 FR](https://creativecommons.org/licenses/by/4.0/deed.fr)). Potete contribuire liberamente alla sua reedazione.

La  [versione francese](https://github.com/LINCnil/Guide-RGPD-du-developpeur) è la versione autentica di questa guida.

## Questa guida è solo per sviluppatori?

Questa guida è intesa principalmente per sviluppatori, sia che lavorino da soli che in team, per i team leader, per i fornitori di servizi ma anche per chiunque sia interessato allo sviluppo web o di software applicativi.

La guida contiene indicazioni e buone pratiche, e pertanto fornisce delle chiavi utili per comprendere il GDPR a ogni stakeholder, quale che sia la dimensione della sua organizzazione. La guida può anche stimolare la discussione e lo sviluppo di pratiche all’interno delle organizzazioni e nelle relazioni con i clienti.

## Che cosa contiene la guida?

Questa guida è divisa in **16 schede tematiche** che coprono la maggior parte delle necessità degli sviluppatori in ciascuno stadio di progetto, dalla preparazione dello sviluppo all’uso di analytics.

Il Regolamento Generale per la Protezione dei Dati Personali (GDPR) specifica che la protezione dei diritti e delle libertà delle persone fisiche richiede **“l'adozione   di misure tecniche e organizzative adeguate per garantire il rispetto delle disposizioni del presente regolamento”** (Considerando 78).

La determinazione di tali misure è necessariamente **collegate al contesto delle operazioni di trattamento poste in essere**, e il Titolare del trattamento (l’entità pubblica o privata che tratta i dati personali) deve pertanto assicurare la sicurezza dei dati che è chiamato a trattare.

Le buone pratiche di questa guida, pertanto, **non intendono coprire tutte le richieste dei regolamenti né intendono essere prescrittive**, ma forniscono un primo livello di misure per affrontare i problemi di sicurezza dei dati negli sviluppi IT che riguardano il trattamento di dati personali. A seconda della natura dei trattamenti, in alcuni casi potrà essere necessario implementare misure aggiuntive al fine di rispondere pienamente ai requisiti di legge. 

## Sommario

0. [Sviluppa in linea con il GDPR](#Scheda_n°0_:_Sviluppa_in_linea_con_il_GDPR)

1. [Individua i dati personali](#Scheda_n°1_:_Individua i dati personali)

2. [Prepara lo sviluppo](#Scheda_n°2_:_Prepara_lo_sviluppo)

3. [Sviluppa in un ambiente sicuro](#Scheda_n°3_:_Sviluppa_in_un_ambiente_sicuro)

4. [Gestisci il codice sorgente](#Scheda_n°4_:_Gestisci_il_codice_sorgente)

5. [Fai scelte architetturali informate](#Scheda_n°5_:_Fai_scelte_architetturali_informate)

6. [Securing your websites, applications and servers](#Sheet_n°6_:_Securing_your_websites,_applications_and_servers)

7. [Minimize data collection](#Sheet_n°7_:_Minimize_data_collection)

8. [Manage user profiles](#Sheet_n°8_:_Manage_users_profiles)

9. [Control your libraries and SDKs](#Sheet_n°09_:_Control_your_libraries_and_SDKs)

10. [Ensure the quality of the code and its documentation](#Sheet_n°10_:_Ensure_quality_of_the_code_and_its_documentation)

11. [Test your applications](#Sheet_n°11_:_Test_your_applications)

12. [Inform users](#Sheet_n°12_:_Inform_users)

13. [Prepare to exercise people's rights](#Sheet_n°13_:_Prepare_for_the_exercise_of_people_rights)

14. [Define a data retention period](#Sheet_n°14_:_Define_a_data_retention_period)

15. [Take into account the legal basis in the technical implementation](#Sheet_n°15_:_Take_into_account_the_legal_bases_in_the_technical_implementation)

16. [Use analytics on your websites and applications](#Sheet_n°16:_Use_analytics_on_your_websites_and_applications)



## Come posso contribuire a questa guida?

**Questa guida è disponibile in due versioni**:

* Una [versione web sul sito di CNIL](http://www.cnil.fr/en/rgpd-developers-guide) e [nel tab "Releases"](https://github.com/LINCnil/GDPR-Developer-Guide/releases) di questo repository;
* Questa [versione GitHub](https://github.com/LINCnil/GDPR-Developer-Guide), che offre a chiunque la possibilità di contribuire.

**Il contributo si articola in alcuni passi**:

* Registrati su GitHub;
* Vai alla pagina di progetto
* Puoi:
    * usare il tab "Issue" per aprire commenti o partecipare alla discussione
    * Usare l’opzione "Fork" per apportare le tue modifiche e proporre la loro inclusione tramite il bottone "Pull Requests".

**Le tue proposte di contributo verranno esaminate da CNIL prima della pubblicazione**. La versione web della Guida al GDPR per sviluppatori sarà aggiornata regolarmente.

## Uso


Per rilasciare tu stesso una copia di questo repository, puoi usare **Pandoc**. Questo strumento di aiuta a convertire le schede in un unico documento docx, odt o HTML.

Puoi trovare le istruzioni su come installare Pandoc [qui]( https://pandoc.org/installing.html)

* **Per generare un file .docx**:

```bash
pandoc -s --toc --toc-depth=1 -o Guide_GDPR_sviluppatori.docx [0-9][0-9]*.md
```

* **Per generare un file .odt**:

```bash
pandoc -s --toc --toc-depth=1 -o Guide_GDPR_sviluppatori.odt [0-9][0-9]*.md
```

* **To generare un file .html file**:

```bash
pandoc -s --template="templates/mytemplate.html" -H templates/pandoc.css -o index.html README.md [0-9][0-9]*.md
```
