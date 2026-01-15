# NeverLost v1.0 — Observer Edition  
**Scanner Forense de Soberania Digital Pessoal** • *Personal Digital Forensics for Normal People*  

> **Sua bagunça nunca mais perdida.**  
NeverLost cria um **mapa offline** do seu PC: varre seus discos (sem mover/apagar nada) e gera um **relatório HTML** + um **banco incremental (SQLite)** para você entender **onde está o peso**, **o que está duplicado** e **o que está “sumindo”** com o tempo.

![UI do NeverLost](docs/screenshots/ui_main.png)

---

## O que ele faz (em 30 segundos)
- ✅ **100% offline** (nada vai pra nuvem)
- ✅ **Read-only** (não move, não apaga, não altera arquivos)
- ✅ **Varre discos automaticamente** (ou você escolhe quais)
- ✅ Gera um **relatório HTML** fácil de ler
- ✅ Mantém um **banco incremental** (re-scans ficam mais rápidos / “memória” local)
- ✅ Marca **MISSING** (itens que estavam e não estão mais)

![Relatório HTML](docs/screenshots/report_top.png)

---

## Para quem é
- Quem tem HD/SSD lotado e vive no “cadê aquele arquivo?”
- Quem tem muitos discos (internos, externos, pendrives)
- Quem quer **soberania**: organização e diagnóstico **sem nuvem**
- Quem quer uma “perícia do caos” antes de mexer em pastas e backups

---

## Como usar (modo recomendado)
1) Baixe a **Observer Edition (One-Click, Windows)** no Gumroad (EXE pronto)  
2) Abra o app, escolha a pasta de saída (onde ficam **relatório + DB**)  
3) Marque **“Iniciar análise em TODOS os discos automaticamente”**  
4) Clique em **Iniciar análise**  
5) Ao finalizar, abra o arquivo: `relatorio_mapa_do_caos.html`

![Como funciona](docs/screenshots/how_it_works.png)

### “Mas eu quero escolher os discos…”
- Desmarque “Todos os discos”  
- Marque só os discos desejados (checkboxes)

---

## O que é gerado na pasta de saída
- `relatorio_mapa_do_caos.html` → relatório visual (abre no navegador)
- `resumo.json` → resumo em JSON (bom pra automações e IA)
- `neverlost.db` (SQLite) → memória incremental / histórico do mapa
- logs → progresso e auditoria

---

## Privacidade e segurança
- O NeverLost roda **localmente**, não envia dados.
- É **OBSERVE_ONLY / read-only**: ele **não altera** seus arquivos.
- Auto-throttle: reduz agressividade quando o ritmo/temperatura pede (protege máquina e disco).

---

## Repositório x Produto
Este repositório é a “vitrine técnica” (código + docs + build).  
A versão vendida é a **Observer Edition (One-Click, EXE pronto + pacote organizado)**.

**Gumroad:** veja a página do produto (link no perfil / descrição).  

---

## Build (para devs)
> Se você só quer usar, ignore esta parte e pegue o EXE no Gumroad.

### Windows (PyInstaller)
1) Instale Python 3.10+  
2) Rode:
```bat
build\build_windows.bat
```
3) O executável sai em `dist\NeverLost_Observer.exe`

---

## Roadmap (versões futuras)
- v1.1: botão **“Abrir relatório”** automático pós-run
- v1.2: relatório com “Top pastas” mais completo
- v2 (PRO): ações guiadas (limpeza/organização assistida), regras de organização e automações do ecossistema EddY

---


## Links oficiais

- Gumroad (download do EXE / versão vendável): https://srdarth.gumroad.com/l/NeverLost
- X / atualizações e suporte: https://x.com/eddysleite
- GitHub (código-fonte / issues): https://github.com/EddysLeite/NeverLost-ObserverEdition

## Exemplo de relatório (sem dados pessoais)

Este repositório inclui um exemplo **sanitizado** em `examples/`:
- `examples/sample_report_redacted.html`
- `examples/sample_resumo_redacted.json`

> Observação: o NeverLost real gera relatórios com caminhos do seu PC. Para publicar prints/relatórios, use sempre versões redatadas.


## Licença
MIT (veja `LICENSE.txt`).

## Contato / suporte
- X: **@eddysleite**
