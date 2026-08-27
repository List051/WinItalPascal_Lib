# WinItalPascal

Libreria Utility per applicazioni WinForms in VB.NET (.NET Framework 4.8).

WinItalPascal semplifica lo sviluppo di applicazioni desktop offrendo utility pronte per:

* Gestione DataGridView
* Connessioni Database SQL Server
* Personalizzazione Form
* Effetti grafici
* Popup e notifiche
* Gestione configurazioni
* Logging automatico

---

# 🎬 Demo Video

Guarda la demo completa della libreria:

📺 **YouTube Demo**
[https://youtu.be/BsjiVc-j8qs](https://youtu.be/BsjiVc-j8qs)

[Visualizza la pagina](https://htmlpreview.github.io/?https://github.com/List051/WinTest_Framework/blob/main/Video.html)

---

# 📦 Installazione

Installazione tramite NuGet Package Manager:

```powershell
Install-Package WinItalPascal
```

Oppure tramite Visual Studio:

```text
Tools → NuGet Package Manager → Manage NuGet Packages
```

Cerca:

```text
WinItalPascal
```

---

# 🗄️ Connection String

La libreria utilizza una connection string chiamata obbligatoriamente:

```text
MiaConnessione
```

Da inserire nel file:

```text
App.config
```

Esempio:

```xml
<connectionStrings>
    <add name="MiaConnessione"
         connectionString="Data Source=SERVER;
         Initial Catalog=DBClienti;
         Integrated Security=True;
         TrustServerCertificate=True"
         providerName="System.Data.SqlClient" />
</connectionStrings>
```

### Note

* `MiaConnessione` deve esistere nel file App.config
* `DBClienti` è il database utilizzato negli esempi demo
* Compatibile con SQL Server

---

# 📁 Struttura Libreria

```text
WinItalPascal
│
├── Core
│   ├── ConfigHelper.vb
│   ├── ThemeFonts.vb
│   ├── Colori.vb
│
├── Database
│   ├── DB.vb
│   ├── GridUtility.vb
│	├── DBQry.vb
│	├── GridFilter.vb
│
├── Forms
│   ├── FormHelper.vb
│   ├── FormUtility.vb
│   ├── FadeUtility.vb
│   ├── ScreenUtility.vb
│	
│   
│
├── Logging
│   ├── FrameworkLogger.vb
│   ├── LeggeLog.vb
│	├── LogReader.vb
│   
│
├── Popup
│   ├── PopupForm.vb
│   ├── PopupHelper.vb
```

---

# 🚀 Funzionalità Principali

## 🎨 GridUtility

Utility per la gestione avanzata dei DataGridView.

Funzioni disponibili:

* Inizializzazione automatica DataGridView
* Colorazione automatica colonne
* Evidenziazione righe selezionate
* Evidenziazione testo
* Gestione colori predefiniti
* Conversione testo maiuscolo
* Reset colori griglia
* Ricerca automatica multi-colonna

---

## 🧮 DB

Utility per accesso database SQL Server.

Funzioni disponibili:

* Connessione SQL Server
* ExecuteScalar
* ExecuteNonQuery
* ExecuteReader
* FillDataTable
* FillDataSet
* Query parametrizzate
* Query LIKE automatiche

---

## 🪟 FormHelper

Gestione grafica dei Form WinForms.

Funzioni disponibili:

* Centratura monitor
* Fade-In / Fade-Out
* Apertura form in panel
* Titolo personalizzato
* Gestione form borderless

---

## 📺 ScreenUtility

Utility per il posizionamento dei form.

Funzioni disponibili:

* Centratura automatica monitor
* Gestione schermo attivo

---

## 🌫 FadeUtility

Effetti grafici per controlli e form.

Funzioni disponibili:

* Fade-In
* Fade-Out
* Transizioni UI

---

## 📝 Logging

Sistema di logging automatico integrato.

Funzioni disponibili:

* Scrittura log
* Gestione errori
* Lettura file log
* Apertura log con Notepad
* Pulizia log

---

# 🔧 Esempi di Utilizzo

## Import Libreria

```vb
Imports WinItalPascal
Imports System.Data.SqlClient
Imports System.Threading.Tasks
```

---

# 🪟 Centratura Form e Titolo Personalizzato

```vb
FormHelper.CentraMonitor(Me)

FrmTitolo.CTitolo(
    Me,
    "Demo WinItalPascal"
)
```

---

# 🎨 Inizializzazione DataGridView

```vb
GridUtility.Initialize(DgvTest)
```

---

# 🗄️ Caricamento Dati SQL

```vb
Dim dt = DB.FillDataTable(
    "SELECT TOP 20 * FROM Clienti"
)

DgvTest.DataSource = dt
```

---

# 🎨 Colorazione Grid

```vb
GridUtility.ColoraColonne(
    DgvTest,
    Colori.ColoreTipo.Giallo,
    Colori.ColoreTipo.Azzurro,
    Colori.ColoreTipo.VerdeChiaro
)

GridUtility.ColoraOK(DgvTest)
```

---

# 🔍 Evidenziazione Testo

```vb
GridUtility.EvidenziaTesto(
    DgvTest,
    "ROMA"
)
```

---

# 🟩 Riga Selezionata

```vb
Private Sub BtnColoraRiga_Click(
    sender As Object,
    e As EventArgs
) Handles BtnColoraRiga.Click

    GridUtility.ColoraRigaSelezionata(
        DgvTest,
        Colori.ColoreTipo.Azzurro
    )

End Sub
```

---

# 📌 Popup Informativi

```vb
Dim img As Image = My.Resources.ImgA

PopupHelper.AttachPopup(
    BtnColoraRiga,
    "Colore Riga Selezionata",
    img
)
```

---

# 🔎 Query Parametrizzate LIKE

```vb
Private Sub BtnQuery_Click(
    sender As Object,
    e As EventArgs
) Handles BtnQuery.Click

    Dim dt = DB.QueryLike(
        "SELECT * FROM Clienti
         WHERE Citta LIKE @p1
         AND CAP LIKE @p2
         ORDER BY Cliente",

        TxtCercaP1.Text,
        TxtCercaP2.Text
    )

    DgvTest.DataSource = dt

End Sub
```

---

# 🔢 ExecuteScalar

```vb
Dim totaleClienti = DB.ExecuteScalar(
    "SELECT COUNT(*) FROM Clienti"
)

MessageBox.Show(
    totaleClienti.ToString()
)
```

---

# ⚙️ ConfigHelper

```vb
Dim cs = ConfigHelper.GetConnectionString()

MessageBox.Show(
    cs,
    "Connection String"
)
```

---

# 📝 Lettura File di Log

```vb
MessageBox.Show(
    LogReader.ReadLog(),
    "FILE LOG"
)
```

---

# 📂 Apertura File Log

```vb
LogReader.OpenLog()
```

---

# 🧹 Pulizia File Log

```vb
LogReader.ClearLog()
```

---

# 🎨 Colori Disponibili

```vb
Public Enum ColoreTipo

    Verde = 1
    Bianco = 2
    Nero = 3
    Azzurro = 4
    Giallo = 5
    Oro = 6
    VerdeChiaro = 7
    BluScuro = 8
    VerdeScuro = 9

End Enum
```

---

# 🛠 Compatibilità

* .NET Framework 4.8
* VB.NET WinForms
* SQL Server
* Visual Studio 2019 / 2022

---

# 📚 Progetto Demo

Nel repository è presente anche un progetto demo completo con:

* esempi DataGridView
* query SQL
* popup
* logging
* modifica dati
* ricerca automatica
* form personalizzati

---

# 👨‍💻 Autore

ItalPascal

---

# 📄 Licenza

MIT License

Uso libero per progetti personali e aziendali.
