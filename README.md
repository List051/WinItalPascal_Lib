<p align="center">
  <img src="Logo.png" alt="Ital Pascal Logo" width="220">
</p>

<h1 align="center">WinItalPascal</h1>
<p align="center">
  Libreria di utilità per applicazioni VB.NET WinForms


<!-- ========================= -->
<!--   BADGE - MANUAL BUILDER  -->
<!-- ========================= -->

<div align="center">
  <strong>📘 WinItalPascal_ManualBuilder</strong>
</div>

<p align="center">

  <a href="https://github.com/List051/WinItalPascal_ManualBuilder">
    <img src="https://img.shields.io/github/stars/List051/WinItalPascal_ManualBuilder?style=for-the-badge" alt="MB Stars">
  </a>

  <a href="https://github.com/List051/WinItalPascal_ManualBuilder">
    <img src="https://img.shields.io/github/forks/List051/WinItalPascal_ManualBuilder?style=for-the-badge" alt="MB Forks">
  </a>

  <a href="https://github.com/List051/WinItalPascal_ManualBuilder/issues">
    <img src="https://img.shields.io/github/issues/List051/WinItalPascal_ManualBuilder?style=for-the-badge" alt="MB Issues">
  </a>

  <a href="https://github.com/List051/WinItalPascal_ManualBuilder/commits/main">
    <img src="https://img.shields.io/github/last-commit/List051/WinItalPascal_ManualBuilder?style=for-the-badge" alt="MB Last Commit">
  </a>

  <a href="https://github.com/List051/WinItalPascal_ManualBuilder/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/List051/WinItalPascal_ManualBuilder?style=for-the-badge" alt="MB License">
  </a>

</p>

<!-- SEPARATORE -->
<div align="center" style="font-size:28px; margin: 10px 0;">⬤</div>

<!-- ========================= -->
<!--   BADGE - LIBRERIA VB.NET -->
<!-- ========================= -->

<div align="center">
  <strong>🧩 WinItalPascal_Lib</strong>
</div>

<p align="center">

  <!-- NuGet -->
  <a href="https://www.nuget.org/packages/WinItalPascal">
    <img src="https://img.shields.io/nuget/v/WinItalPascal?style=for-the-badge" alt="NuGet Version">
  </a>

  <a href="https://www.nuget.org/packages/WinItalPascal">
    <img src="https://img.shields.io/nuget/dt/WinItalPascal?style=for-the-badge" alt="NuGet Downloads">
  </a>

  <!-- GitHub -->
  <a href="https://github.com/List051/WinItalPascal_Lib">
    <img src="https://img.shields.io/github/stars/List051/WinItalPascal_Lib?style=for-the-badge" alt="Lib Stars">
  </a>

  <a href="https://github.com/List051/WinItalPascal_Lib">
    <img src="https://img.shields.io/github/forks/List051/WinItalPascal_Lib?style=for-the-badge" alt="Lib Forks">
  </a>

  <a href="https://github.com/List051/WinItalPascal_Lib/issues">
    <img src="https://img.shields.io/github/issues/List051/WinItalPascal_Lib?style=for-the-badge" alt="Lib Issues">
  </a>

  <a href="https://github.com/List051/WinItalPascal_Lib/commits/main">
    <img src="https://img.shields.io/github/last-commit/List051/WinItalPascal_Lib?style=for-the-badge" alt="Lib Last Commit">
  </a>

  <a href="https://github.com/List051/WinItalPascal_Lib/blob/main/License.txt">
    <img src="https://img.shields.io/github/license/List051/WinItalPascal_Lib?style=for-the-badge" alt="Lib License">
  </a>

</p>

<!--   FINE BADGE - LIBRERIA VB.NET -->
---


WinItalPascal è una libreria di componenti e utility pensata per velocizzare lo sviluppo di applicazioni desktop realizzate con:

VB.NET
Windows Forms
.NET Framework 4.8

La libreria raccoglie funzioni comuni normalmente riscritte in ogni progetto:

gestione database SQL Server
gestione avanzata DataGridView
report RDLC
gestione form
logging
popup
utility grafiche

L'obiettivo è fornire codice riutilizzabile, ordinato e facilmente manutenibile.

📌 Versioni

## **2.0.6**
- Aggiunta `IPMessageBox`, alternativa personalizzabile al `MessageBox` standard di Windows Forms.
- ...
2.0.5
Corretta distribuzione DLL NuGet
Migliorata gestione dipendenze NuGet
Compatibilità migliorata con progetti esistenti

Nota importante

Durante il debug in Visual Studio può comparire l'avviso PInvokeStackImbalance relativo a Microsoft.ReportViewer.Common durante l'esportazione PDF.

Questo è un Managed Debugging Assistant del debugger e non indica un errore della libreria WinItalPascal.

Se il PDF viene generato correttamente, è possibile disabilitare l'interruzione dell'avviso da:

Debug → Eccezioni → Managed Debugging Assistants → PInvokeStackImbalance

2.0.0
Prima release pubblica
📦 Struttura della Libreria
WinItalPascal
│
├── Database
│   └── DB
│
├── Grid
│   └── DataGVLoad
│
├── Reports
│   ├── ReportManager
│   └── ReportImpostazioni
│
├── Forms
│
├── Logging
│   └── FrameworkLogger
│
└── Popup
| IPMessageBox 

📦 Installazione

Installazione tramite NuGet:

Install-Package WinItalPascal


Oppure tramite Visual Studio:

Gestione pacchetti NuGet → Cerca → WinItalPascal

🚀 Funzionalità disponibili
🗄 Database

Modulo per la gestione di SQL Server.

Classe principale: DB

Funzioni disponibili:

GetConnection
ExecuteScalar
ExecuteNonQuery
ExecuteReader
FillDataTable
FillDataSet
query parametrizzate
gestione connessioni

📚 Documentazione: README_Database.md

📊 GridUtility

Gestione avanzata di DataGridView.

Classe principale: DataGVLoad

Funzioni disponibili:

caricamento dati
configurazione automatica colonne
formattazione
gestione colori
ricerca
conversione testo
gestione eventi

📚 Documentazione: README_GridUtility.md

📄 Report RDLC

Gestione centralizzata dei report.

Classi principali:

ReportManager
ReportImpostazioni

Funzioni disponibili:

caricamento report RDLC
collegamento DataTable
gestione ReportViewer
stampa
esportazione PDF
query SQL
query parametrizzate

📚 Documentazione: README_Reports.md

🪟 Forms Utility

Utility dedicate ai Windows Form.

Funzioni disponibili:

apertura form
gestione titoli
Fade
gestione schermate
gestione dimensionamento
modalità FullScreen

📚 Documentazione: README_Forms.md

📝 Logging

Sistema integrato di registrazione degli eventi.

Classi principali:

FrameworkLogger
LogLeggiScrivi

Funzioni disponibili:

log eventi
registrazione errori
gestione file di log

📚 Documentazione: README_Logging.md

🔔 Popup e Utility

Gestione di finestre informative e messaggi personalizzati.

Comprende:

PopupHelper
PopupForm
utility grafiche

📚 Documentazione: README_Popup.md

⚙️ Configurazione Database

La libreria utilizza la connection string:

MiaConnessione

Esempio
<connectionStrings>
    <add name="MiaConnessione"
         connectionString="Data Source=SERVER;
                           Initial Catalog=DBClienti;
                           Integrated Security=True;
                           TrustServerCertificate=True"
         providerName="System.Data.SqlClient"/>
</connectionStrings>

🎬 Video, esempi e documentazione

Per guide dettagliate, video dimostrativi, documentazione PDF ed esempi pratici è disponibile il repository dedicato:

👉 WinItalPascal_Help https://github.com/List051/WinItalPascal_Help

All'interno del repository è disponibile il file index.html, che raccoglie in un'unica pagina:

🎬 video dimostrativi
📄 documentazione PDF
💻 esempi pratici
📚 guide all'utilizzo della libreria

Il repository WinItalPascal contiene il codice e le funzionalità della libreria, mentre WinItalPascal_Help è il punto di riferimento per la documentazione e gli esempi.

💻 Repository GitHub

Repository ufficiale:

👉 https://github.com/List051/WinItalPasca_Lib

📦 Pacchetto NuGet

Il pacchetto WinItalPascal è disponibile su NuGet:

👉 https://www.nuget.org/packages/WinItalPascal

📚 Documentazione

I principali documenti presenti nel progetto sono:

README.md
README_Database.md
README_GridUtility.md
README_Reports.md
README_Forms.md
README_Logging.md
README_Popup.md
CHANGELOG.md

Per la documentazione completa, gli esempi e i video dimostrativi:

👉 WinItalPascal_Help

> `WinTest-SenzaVINCOLI` è un progetto dimostrativo e non rappresenta la
> libreria completa. Il suo scopo è mostrare come integrare e utilizzare
> WinItalPascal in un'applicazione Windows Forms.



Il progetto [WinSenzaVincoli](https://github.com/List051/WinTest-SenzaVINCOLI)
mostra come utilizzare WinItalPascal all'interno di un'applicazione desktop
reale sviluppata con VB.NET, Windows Forms e .NET Framework 4.8.



🛠 Compatibilità
.NET Framework 4.8
VB.NET WinForms
SQL Server
Visual Studio 2019
Visual Studio 2022
🤝 Contribuire


WinItalPascal è un progetto in continua evoluzione e i contributi sono benvenuti.

Se utilizzi la libreria e hai trovato un problema, hai un'idea per migliorarla oppure vuoi proporre una nuova funzionalità, puoi contribuire in diversi modi:

🐛 Segnalare un bug aprendo una Issue.
💡 Proporre una nuova funzionalità o un miglioramento.
🔧 Correggere un problema o migliorare il codice esistente.
📚 Migliorare la documentazione o gli esempi.
🧪 Proporre nuovi casi d'uso che possano essere utili agli sviluppatori che utilizzano WinItalPascal.
🔀 Aprire una Pull Request con le proprie modifiche.
📌 Linee guida

WinItalPascal nasce con l'obiettivo di fornire utility semplici, riutilizzabili e facilmente integrabili in applicazioni VB.NET WinForms.

Per questo motivo, i contributi dovrebbero preferibilmente:

mantenere la compatibilità con le versioni supportate del framework;
seguire lo stile e la struttura già presenti nel progetto;
essere semplici da comprendere e mantenere;
includere, quando necessario, una descrizione del funzionamento o un esempio pratico.


# 🔗 Link utili

## 📚 Documentazione della libreria WinItalPascal

- [📘 Documentazione Tecnica (*.md)](https://github.com/List051/WinItalPascal_Lib/tree/main/Documentation)
- [📄 Manuali PDF della libreria](https://github.com/List051/WinItalPascal_Lib/tree/main/Help/pdf)

---

## 🎬 Video dimostrativi

- [🎥 Video Esempi – WinVideoShowcase](https://list051.github.io/WinVideoShowcase/)
- [📺 Canale YouTube](https://www.youtube.com/@iaoraGo)
- [🎞️ Playlist completa WinItalPascal](https://www.youtube.com/watch?v=UboNebA_Irs&list=PLqYE2xAtyfEAiNY4qC2LeJJuCJPyUScXL)

---

📄 Licenza

MIT License

WinItalPascal può essere utilizzato in applicazioni personali, aziendali e commerciali nel rispetto dei termini della licenza MIT.

WinItalPascal – Utility Library for VB.NET WinForms

Versione documentazione: 2.0.6

---

<div align="center">
  <h2>⭐ Come supportare il progetto</h2>
  <p>Se questo progetto ti è utile, puoi supportarlo con un semplice gesto:</p>

  <!-- Pulsante Star -->
  <a href="https://github.com/List051/WinItalPascal_Lib">
    <img src="https://img.shields.io/github/stars/List051/WinItalPascal_Lib?style=social" alt="Star this repo">
  </a>

  <!-- Pulsante Fork -->
  <a href="https://github.com/List051/WinItalPascal_Lib/fork">
    <img src="https://img.shields.io/github/forks/List051/WinItalPascal_Lib?label=fork&style=social" alt="Fork this repo">
  </a>

  <p>Mettere una ⭐ o fare un Fork aiuta il progetto a crescere e permette ad altri sviluppatori di scoprirlo.</p>

  <br>

  <!-- Pulsante Follow autore -->
  <p>Vuoi restare aggiornato sui nuovi progetti?</p>

  <a href="https://github.com/List051">
    <img src="https://img.shields.io/github/followers/List051?label=Follow%20%40List051&style=social" alt="Follow @List051">
  </a>

  <p>Grazie per il tuo supporto!</p>
</div>
