# OctoPrint-DetailedProgress German

A plugin that sends M117 commands to the printer to display the progress of the print job being currently streamed. The message to display can be configured (some placeholders included).
![Example ETA](https://i.imgur.com/ocBp152.jpg)
![Example ETL](https://i.imgur.com/oJiMm2p.jpg)
![Example Percent](https://i.imgur.com/McaCNsx.jpg)

## Setup

Manuelle installieren mit dem PluginManager. URL ist:

    https://github.com/DeDouby/OctoPrint-DetailedProgress-German/archive/master.zip
 

## Configuration

``` yaml
plugins:
  detailedprogress:
    # Number of seconds (minimum) to rotate the messages
    time_to_change: 10
    eta_strftime: "%H:%M:%S Day %d"
    etl_format: "{hours:02d}:{minutes:02d}:{seconds:02d}"
    # Messages to display. Placeholders:
    # - completion : The % completed
    # - printTimeLeft : A string in the format "HH:MM:SS" with how long the print still has left
    # - ETA : The date and time formatted in "%H:%M:%S Day %d" that the print is estimated to be completed
    # - filepos: The current position in the file currently being printed
    messages:
      - "{completion:.2f}% complete"
      - "ETL: {printTimeLeft}"
      - "ETA: {ETA}"
```
