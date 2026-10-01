# deploy/ — the files uploaded to GitHub by hand

The public map (`index.html`) is published from **Workbench → Publish** and is not here.
Everything in this folder is the current copy of a file that has to be uploaded manually:
download the folder, then on GitHub use **Add file → Upload files → Commit changes**.

| File | What it is | Upload when |
|---|---|---|
| `workbench.html` | The Workbench, bundled into one file. Opens only for a W5 administrator. | After Workbench changes |
| `inspector.html` | The Inspector, bundled. Opens only for a W5 administrator. | After Inspector changes |
| `beta.html` | Turns on feedback mode, then opens the map. | Once |
| `.nojekyll` | Tells GitHub Pages to serve files as they are. | Once |

## Safety

- Both internal pages show the admin gate first. Anyone who is not an administrator is sent to the map.
- The server decides what each person may read or write, whatever page they use: a non-admin gets the
  viewer-level data only and cannot save. So a copy of these pages on a public repository gives
  nothing away by itself.
- The server files (`server/w5-apps-script/*.gs`) are never uploaded to GitHub. They are pasted into
  Apps Script and deployed as a **New version**.
