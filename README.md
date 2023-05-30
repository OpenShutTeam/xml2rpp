# XML to RPP
## _Software for convert Adobe Premiere pro project (XML file) to REAPER project (RPP)_

[![N|Solid](https://img.shields.io/github/v/tag/OpenShutTeam/xml2rpp?color=blueviolet&label=Last%20version&style=plastic)](https://github.com/OpenShutTeam/xml2rpp/releases) [![N|Solid](https://img.shields.io/badge/Mac%20OS-10.14.6+-green?style=plastic)](https://github.com/OpenShutTeam/xml2rpp/releases) [![N|Solid](https://img.shields.io/badge/Win%20-10+-green?style=plastic)](https://github.com/OpenShutTeam/xml2rpp/releases) [![N|Solid](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAAAeCAYAAADaW7vzAAAACXBIWXMAAC4jAAAuIwF4pT92AAAJEGlUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iQWRvYmUgWE1QIENvcmUgNy4yLWMwMDAgNzkuNTY2ZWJjNSwgMjAyMi8wNS8wOS0wNzoyMjoyOSAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczpkYz0iaHR0cDovL3B1cmwub3JnL2RjL2VsZW1lbnRzLzEuMS8iIHhtbG5zOnhtcE1NPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvbW0vIiB4bWxuczpzdEV2dD0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL3NUeXBlL1Jlc291cmNlRXZlbnQjIiB4bWxuczpzdFJlZj0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL3NUeXBlL1Jlc291cmNlUmVmIyIgeG1sbnM6cGhvdG9zaG9wPSJodHRwOi8vbnMuYWRvYmUuY29tL3Bob3Rvc2hvcC8xLjAvIiB4bXA6Q3JlYXRvclRvb2w9IkFkb2JlIFBob3Rvc2hvcCAyMy40IChXaW5kb3dzKSIgeG1wOkNyZWF0ZURhdGU9IjIwMjMtMDQtMDNUMjM6NTc6MjYrMDM6MDAiIHhtcDpNZXRhZGF0YURhdGU9IjIwMjMtMDQtMDNUMjM6NTc6NDArMDM6MDAiIHhtcDpNb2RpZnlEYXRlPSIyMDIzLTA0LTAzVDIzOjU3OjQwKzAzOjAwIiBkYzpmb3JtYXQ9ImltYWdlL3BuZyIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDphMjIyYjViNy1jZDkyLTZjNDQtOGY0ZC00ZTZlNzA5OWE1YWMiIHhtcE1NOkRvY3VtZW50SUQ9ImFkb2JlOmRvY2lkOnBob3Rvc2hvcDo0MDg3OGRmNC1mNDE2LTgyNGEtODVjOS1kZTgxNzgxOGE0NmMiIHhtcE1NOk9yaWdpbmFsRG9jdW1lbnRJRD0ieG1wLmRpZDoyZDZjNDc2ZS0zYTU0LTNlNDQtYjM0Mi1jYmJkMGM5NmFlOWYiIHBob3Rvc2hvcDpDb2xvck1vZGU9IjMiPiA8eG1wTU06SGlzdG9yeT4gPHJkZjpTZXE+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJjcmVhdGVkIiBzdEV2dDppbnN0YW5jZUlEPSJ4bXAuaWlkOjJkNmM0NzZlLTNhNTQtM2U0NC1iMzQyLWNiYmQwYzk2YWU5ZiIgc3RFdnQ6d2hlbj0iMjAyMy0wNC0wM1QyMzo1NzoyNiswMzowMCIgc3RFdnQ6c29mdHdhcmVBZ2VudD0iQWRvYmUgUGhvdG9zaG9wIDIzLjQgKFdpbmRvd3MpIi8+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJzYXZlZCIgc3RFdnQ6aW5zdGFuY2VJRD0ieG1wLmlpZDpmMDkwZjMxZi03NmViLTkxNDEtOGY4OC01ZDI1YzU2Mzc4YzUiIHN0RXZ0OndoZW49IjIwMjMtMDQtMDNUMjM6NTc6NDArMDM6MDAiIHN0RXZ0OnNvZnR3YXJlQWdlbnQ9IkFkb2JlIFBob3Rvc2hvcCAyMy40IChXaW5kb3dzKSIgc3RFdnQ6Y2hhbmdlZD0iLyIvPiA8cmRmOmxpIHN0RXZ0OmFjdGlvbj0iY29udmVydGVkIiBzdEV2dDpwYXJhbWV0ZXJzPSJmcm9tIGFwcGxpY2F0aW9uL3ZuZC5hZG9iZS5waG90b3Nob3AgdG8gaW1hZ2UvcG5nIi8+IDxyZGY6bGkgc3RFdnQ6YWN0aW9uPSJkZXJpdmVkIiBzdEV2dDpwYXJhbWV0ZXJzPSJjb252ZXJ0ZWQgZnJvbSBhcHBsaWNhdGlvbi92bmQuYWRvYmUucGhvdG9zaG9wIHRvIGltYWdlL3BuZyIvPiA8cmRmOmxpIHN0RXZ0OmFjdGlvbj0ic2F2ZWQiIHN0RXZ0Omluc3RhbmNlSUQ9InhtcC5paWQ6YTIyMmI1YjctY2Q5Mi02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)](https://denial.diaka.ua/donate)

EN: Support for operating systems Mac OS 10.14.6, Windows 10, 11 and above.
UA: Підтримка операційних систем Mac OS 10.14.6, Windows 10, 11 та вище.


## Functional
language: еnglish, українська, polski.

EN:
- Timeline support (tracks, position of fragments and their trimming)
- Support for xml files created in Adobe Premiere pro on Mac and Win systems
- RPP file creation support for Mac and Win systems
- Support for disabled fragments (only for those who made a voluntary charitable contribution for the development of the project and received a key)
- Support for fades (only for those who made a voluntary charitable contribution for the development of the project and received a key)
- Support for the volume level of fragments (only for those who made a voluntary charitable contribution for the development of the project and received a key)

UA: 
- Підтримка таймлайну (доріжки, позиція фрагментів та їх обрізка)
- Підтримка файлів xml створених в Adobe Premiere pro на системі Mac та Win
- Підтримка створення файлу RPP для систем Mac та Win
- Підтримка вимклених фрагментів (тільки для тих хто зрибив добровільний благодійний внесок для розвитку проєкту та отримав ключ)
- Підтримка фейдів (тільки для тих хто зрибив добровільний благодійний внесок для розвитку проєкту та отримав ключ)
- Підтримка рівня гучності фрагментів (тільки для тих хто зробив добровільний благодійний внесок для розвитку проєкту та отримав ключ)

## Donate
EN: This project is not commercial, all collected funds go to software development. Voluntary charitable contribution is not mandatory but strongly influences the author's motivation. I will be very glad for your support. Thank you!

UA: Даний проект не є комерційним, усі зібрані кошти йдуть на розвиток програмного забезпечення. Добровільний благодійний внесок не є обов'язковим але потужно впливає на мотивацію автора. Буду дуже радий вашій підтримці. Дякую!

## Support
UA: Якщо у вас є пропозиції або зауваження надсилайте на e-mail openshutteam@ukr.net При можливості додайте скріншот або посилання на youtube.

EN: If you have suggestions or comments, send them to openshutteam@ukr.net If possible, add a screenshot or a youtube link.

## License
EN: Information about the license is added in this repository file LICENSE.txt

UA: Інформація про ліцензію додається в даному репозиторії файл LICENSE.txt
