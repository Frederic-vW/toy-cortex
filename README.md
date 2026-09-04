# EEG-like Oscillations from Spiking Neurons

An undergraduate neuroscience practical: build a network of Izhikevich spiking
neurons and show how synchronised excitatory/inhibitory activity produces
EEG-like oscillations, analysed with power spectra and related to standard
EEG frequency bands.

Notebook: [`content/eeg-rhythms-jlite.ipynb`](content/eeg-rhythms-jlite.ipynb)

Runs entirely in the browser via [JupyterLite](https://jupyterlite.readthedocs.io/)
(Pyodide kernel) — no local Python install needed. Only `numpy`, `scipy`, and
`matplotlib` are used, all of which are available in the Pyodide kernel.

## Deploying to GitHub Pages

1. Push this folder to a new GitHub repository.
2. In the repo settings, go to **Pages** and set **Source** to **GitHub Actions**.
3. Push to `main` (or run the workflow manually from the **Actions** tab) — the
   `.github/workflows/deploy.yml` workflow builds the JupyterLite site and
   deploys it to Pages automatically.
4. The site (including the notebook, launchable directly in-browser) will be
   available at `https://<username>.github.io/<repo-name>/lab/index.html?path=eeg-rhythms-jlite.ipynb`
   (or via the JupyterLite tree/retro view at the site root).

## Local build (optional, to preview before pushing)

```bash
pip install -r requirements.txt
jupyter lite build --contents content --output-dir _output
jupyter lite serve --output-dir _output
```
