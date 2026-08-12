# Estetica Master — Landing Page

Pagina standalone, pronta per essere pubblicata su GitHub Pages (o Netlify/Vercel) e collegata a un dominio GoDaddy.

## Cosa contiene
- `index.html` — pagina unica, HTML/CSS/JS inline (nessuna dipendenza esterna oltre Google Fonts, Wistia, YouTube thumbnails, Calendly link).
- Logo incluso come immagine base64 (nessun file esterno da gestire).

## Deploy su GitHub Pages (gratis)

1. Crea una repo su GitHub, es. `estetica-master-landing`.
2. Carica `index.html` nella root della repo (via web upload o `git push`).
3. Vai su **Settings → Pages** della repo.
4. In "Build and deployment" scegli **Deploy from a branch**, branch `main`, folder `/ (root)`.
5. Dopo 1-2 minuti la pagina sarà live su `https://<tuo-username>.github.io/estetica-master-landing/`.

## Collegare il dominio GoDaddy

### Opzione A — dominio radice (es. esteticamaster.it)
Su GoDaddy, sezione DNS del dominio, aggiungi:
- Record A → `185.199.108.153`
- Record A → `185.199.109.153`
- Record A → `185.199.110.153`
- Record A → `185.199.111.153`

(sono gli IP ufficiali di GitHub Pages)

### Opzione B — sottodominio (es. www.esteticamaster.it)
- Record CNAME `www` → `<tuo-username>.github.io`

Poi su GitHub, in **Settings → Pages → Custom domain**, inserisci il dominio e attendi la verifica DNS + certificato SSL automatico (Let's Encrypt, gestito da GitHub).

## Note
- Il video Wistia e i testimonial YouTube funzionano invariati: sono embed pubblici, non serve nulla lato hosting.
- Il pulsante CTA punta a Calendly (`calendly.com/davide-tessaro-business/30min`) — invariato.
- Se vuoi il form di lead capture collegato a GHL/Make.com invece del solo link Calendly, si aggiunge come snippet JS separato che chiama un webhook.
