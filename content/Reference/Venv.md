---
{"publish":true,"title":"🐍 Venv","tags":["python"],"PassFrontmatter":true}
---

Set up environments in [Python].

### Activate

```bash
source env/bin/activate
```

### Deactivate

```bash
deactivate
```

### Create new environment

```bash
python3 -m venv env
```

### Install dependencies

```bash
pip3 install -r requirements.txt
```

### Make new requirements.txt file

```bash
pip freeze > requirements.txt
```