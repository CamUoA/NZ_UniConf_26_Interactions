[README.md](https://github.com/user-attachments/files/28687608/README.md)
# AI in Finance — Conference Interactions App v4 Production

This production version has:

- Firebase config hard-coded
- No Firebase setup screen for attendees
- Presenter dashboard hidden unless the URL includes `#dashboard` or `#presenter`
- Presenter-controlled stage gating
- University selector and editable role list
- Journey poll
- Use-case wall
- AI opportunity poll

## Links

Audience QR:

```text
https://your-github-pages-url/
```

Presenter dashboard:

```text
https://your-github-pages-url/#dashboard
```

or:

```text
https://your-github-pages-url/#presenter
```

## Presenter flow

1. Open the presenter dashboard using `#dashboard`.
2. Click **Open Profile** while people arrive.
3. Click **Open Journey** during the journey section.
4. Click **Open Use-case** during the use-case discussion.
5. Click **Open Opportunity** near the close.
6. Click **Open All** after the presentation so attendees can complete or update responses.
7. Click **Close Voting** when finished.

## Firebase

This version is already connected to:

```text
nz-uni-fin-conf-26
```

Realtime Database:

```text
https://nz-uni-fin-conf-26-default-rtdb.asia-southeast1.firebasedatabase.app
```

Session path:

```text
sessions/uoa-finance-ai-conference-2026-v3-gated/
```

## Deploy to GitHub Pages

Upload this `index.html` to your GitHub repository root, then enable Pages:

- Settings -> Pages
- Source: Deploy from a branch
- Branch: main
- Folder: / root

## After the event

In Firebase Realtime Database rules, disable writes or delete the database.

Example lock-down rules:

```json
{
  "rules": {
    ".read": true,
    ".write": false
  }
}
```
