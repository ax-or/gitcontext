# 🧪 Tests for `git-ctx`

This directory includes unit and CLI integration tests for the `git-ctx` context-aware Git wrapper.

---

## 📂 Structure

- `test_cli_updated.py` — Primary test suite using `pytest` and `click.testing`

---

## 🧪 How to Run Tests

First, ensure dependencies are installed:

```bash
pip install -e ".[dev]"
```

Then run the test suite:

```bash
pytest -v tests/
```

---

## ✅ Coveragep[TODO]

- ✔️ Context resolution from `project.context`
- ✔️ Prefix override using `-x/--prefix`
- ✔️ Proper fallback to normal `git` mode when `-k/--ctx` is absent
- ✔️ Raw Git passthrough verified when `-k` is missing
- ✔️ Error messages for missing context files

---

## 💡 Notes

- Uses temporary filesystem with `CliRunner().isolated_filesystem()` for safety
- Simulates Git repo layout (`.git/` folder, `project.context`)
- Designed to pass even if Git itself is not configured (focus is on CLI behavior)

---

