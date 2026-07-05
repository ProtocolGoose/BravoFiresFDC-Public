# Owner / Repo Alignment Required

The current public files you uploaded still reference `ProtocolGoose/BravoFiresFDC-Public` in the older v3.x workflow.

The v4.1.3-beta C# app package points to:

```text
https://raw.githubusercontent.com/GooseProtocol/BravoFiresFDC-Public/main/releases/latest.json
```

That means one of these must be true before the public updater will work:

1. The public repo is actually `GooseProtocol/BravoFiresFDC-Public` and these files are pushed there, or
2. The app is patched/rebuilt so `AppPaths.UpdateManifestUrl` points to the real public repo owner/path.

If your actual public repo remains `ProtocolGoose/BravoFiresFDC-Public`, the next private app build should update:

```text
src/BravoFiresFDC.App/AppPaths.cs
```

from:

```text
https://raw.githubusercontent.com/GooseProtocol/BravoFiresFDC-Public/main/releases/latest.json
```

to:

```text
https://raw.githubusercontent.com/ProtocolGoose/BravoFiresFDC-Public/main/releases/latest.json
```
