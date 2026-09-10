
# IPMessageBox

`IPMessageBox` è il componente di `WinItalPascal` utilizzato per visualizzare messaggi, avvisi, errori e richieste di conferma all'interno dell'applicazione.

## Utilizzo

Per utilizzare `IPMessageBox` all'interno di un Form è sufficiente importare il namespace:

```vb
Imports WinItalPascal
```

Dopo aver aggiunto l'import, è possibile utilizzare direttamente `IPMessageBox` senza specificare il namespace completo:

```vb
IPMessageBox.Show(
    "Operazione completata.",
    "Informazione",
    MessageBoxButtons.OK,
    MessageBoxIcon.Information)
```

Non è quindi necessario scrivere:

```vb
WinItalPascal.IPMessageBox.Show(...)
```

### Esempio completo

```vb
Imports WinItalPascal

Public Class Form1

    Private Sub BtnSalva_Click(sender As Object, e As EventArgs) Handles BtnSalva.Click

        Try

            ' Operazione di salvataggio
            SalvaDati()

            IPMessageBox.Show(
                "Salvataggio completato correttamente.",
                "Informazione",
                MessageBoxButtons.OK,
                MessageBoxIcon.Information)

        Catch ex As Exception

            IPMessageBox.Show(
                "ERRORE SALVATAGGIO: " & ex.Message,
                "Errore",
                MessageBoxButtons.OK,
                MessageBoxIcon.Error)

        End Try

    End Sub

End Class
```

## Sintassi

La sintassi di base è analoga a quella di `MessageBox.Show`:

```vb
IPMessageBox.Show(
    testo,
    titolo,
    pulsanti,
    icona)
```

### Parametri

|Parametro|Descrizione|
|---|---|
|`testo`|Testo del messaggio visualizzato|
|`titolo`|Titolo della finestra|
|`pulsanti`|Pulsanti da visualizzare|
|`icona`|Icona associata al messaggio|

## Messaggio informativo

```vb
IPMessageBox.Show(
    "Operazione completata correttamente.",
    "Informazione",
    MessageBoxButtons.OK,
    MessageBoxIcon.Information)
```

## Errore

```vb
Try

    ' Operazione

Catch ex As Exception

    IPMessageBox.Show(
        "ERRORE: " & ex.Message,
        "Errore",
        MessageBoxButtons.OK,
        MessageBoxIcon.Error)

End Try
```

## Avviso

```vb
IPMessageBox.Show(
    "Attenzione: verificare i dati inseriti.",
    "Attenzione",
    MessageBoxButtons.OK,
    MessageBoxIcon.Warning)
```

## Domanda / conferma

```vb
Dim result As DialogResult = IPMessageBox.Show(
    "Vuoi procedere?",
    "Conferma",
    MessageBoxButtons.YesNo,
    MessageBoxIcon.Question)

If result = DialogResult.Yes Then
    ' Procedi
End If
```

## Conferma eliminazione

```vb
Dim result As DialogResult = IPMessageBox.Show(
    "Sei sicuro di voler eliminare il record?",
    "Conferma eliminazione",
    MessageBoxButtons.YesNo,
    MessageBoxIcon.Warning)

If result = DialogResult.Yes Then

    ' Eliminazione del record

End If
```

## Annullamento

```vb
Dim result As DialogResult = IPMessageBox.Show(
    "Vuoi annullare l'operazione?",
    "Conferma",
    MessageBoxButtons.OKCancel,
    MessageBoxIcon.Question)

If result = DialogResult.OK Then
    ' Operazione annullata
End If
```

## `YesNoCancel`

```vb
Dim result As DialogResult = IPMessageBox.Show(
    "Vuoi salvare le modifiche?",
    "Modifiche non salvate",
    MessageBoxButtons.YesNoCancel,
    MessageBoxIcon.Question)

Select Case result

    Case DialogResult.Yes
        ' Salva

    Case DialogResult.No
        ' Non salvare

    Case DialogResult.Cancel
        ' Annulla e rimani nella finestra

End Select
```

## Validazione dei dati

```vb
If String.IsNullOrWhiteSpace(txtNome.Text) Then

    IPMessageBox.Show(
        "Inserire il nome.",
        "Dati mancanti",
        MessageBoxButtons.OK,
        MessageBoxIcon.Warning)

    txtNome.Focus()
    Return

End If
```

## Accesso non consentito

```vb
If Not UtenteAutorizzato Then

    IPMessageBox.Show(
        "Non hai i permessi necessari per eseguire questa operazione.",
        "Accesso negato",
        MessageBoxButtons.OK,
        MessageBoxIcon.Error)

    Return

End If
```

## Errore durante il caricamento

```vb
Try

    CaricaDati()

Catch ex As Exception

    IPMessageBox.Show(
        "ERRORE CARICAMENTO DATI: " & ex.Message,
        "Errore",
        MessageBoxButtons.OK,
        MessageBoxIcon.Error)

End Try
```

## Best practice

Quando si gestisce un'eccezione, è consigliabile mostrare all'utente un messaggio comprensibile e utilizzare `ex.Message` per fornire il dettaglio tecnico dell'errore:

```vb
Try

    ' Operazione

Catch ex As Exception

    IPMessageBox.Show(
        "Si è verificato un errore durante l'operazione." &
        Environment.NewLine &
        Environment.NewLine &
        "Dettaglio: " & ex.Message,
        "Errore",
        MessageBoxButtons.OK,
        MessageBoxIcon.Error)

End Try
```

Per utilizzare `IPMessageBox` utilizza ultima versione:

```vb
Versione 2.0.6 WinItalPascal
```
