# AGENTS.md — perfect-woocommerce

Gemeinsame Instruktionsdatei für alle Agenten (Claude, Codex, Gemini); `CLAUDE.md` ist ein
Symlink hierauf. Globale Regeln: `~/Developer/KI/neo.md`.

**Öffentliches Produkt** (`github.com/greecro/perfect-woocommerce`): Schwesterprojekt von
`perfect-wordpress` mit demselben Aufbau, aber auf WooCommerce-Lasten ausgelegt (größere
PHP- und Redis-Budgets, Cache-Ausnahmen für Warenkorb und Checkout).
Details: [README.md](README.md) (englisch).

## Projektregeln

1. **Öffentliches Repo, fremde Zielgruppe.** Keine IPs, Hostnamen, Domains oder
   Lizenzschlüssel aus Danys Umgebung, auch nicht als Beispiel.
2. **README und Ausgaben bleiben englisch.**
3. **Änderungen gegen `perfect-wordpress` spiegeln.** Die beiden Installer sind bewusst
   parallel gebaut; ein Fix hier, der dort fehlt, macht die Paare unvorhersehbar. Umgekehrt
   gilt dasselbe.
4. **`proxmox-perfect-woocommerce` ruft dieses Repo auf** — bei Änderungen an Prompts oder
   Flags den Wrapper mitprüfen.
5. **Cache darf Warenkorb, Checkout und Konto nie erfassen.** Das ist die eine Stelle, an der
   ein „Performance-Fix" echten Schaden anrichtet — nie ohne Test gegen einen Shop ändern.
6. **Der One-line-Installer zieht direkt von GitHub** — nichts Halbfertiges auf den
   Standard-Branch.
