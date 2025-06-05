# 🧪 Testing `git-ctx`

This directory contains tests for the `git-ctx` CLI tool using `pytest`.

## ✅ Setup

1. Make sure you have installed the tool in dev mode:

```bash
pip install -e .[dev]
```

2. To run the tests:

```bash
pytest -v tests/
```

---

## 📂 Test Descriptions

- `test_context_prefix_with_subproject`: Ensures correct context prefix when both project and subproject are present.
- `test_context_prefix_without_subproject`: Ensures fallback to project-only prefix.
- `test_context_file_missing_key`: Fails gracefully if `project` key is missing.
- `test_checkout_without_branch`: Validates error message when `checkout` is run without a branch name.
- `test_push_with_extra_args`: Checks that extra push flags like `--force` are accepted.
- `test_fuzzy_pick_empty_context`: Fails gracefully if fuzzy pick is attempted in an empty context.

---

## 🛠️ Tip

Use `monkeypatch.chdir(...)` to simulate being inside a Git repo in your tests.
Use `CliRunner()` from `click.testing` to simulate CLI calls without needing subprocess.

Happy testing!
