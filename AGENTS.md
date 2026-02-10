# Styleguide project

## Deploying

1. Commit and push to `main` on GitHub
2. SSH to `thet` and run `~/ritza-styleguide/build-and-deploy.sh`

```bash
git push origin main
ssh thet "cd ~/ritza-styleguide && bash build-and-deploy.sh"
```

## Building locally

```bash
python3 -m venv .venv --clear
.venv/bin/pip install -r requirements.txt
.venv/bin/pip install 'mkdocs>=1.5' 'mkdocs-material>=9'
.venv/bin/mkdocs build
```

Note: `requirements.txt` pins old versions that are incompatible with current Python. The extra pip install line upgrades mkdocs and mkdocs-material to working versions.
