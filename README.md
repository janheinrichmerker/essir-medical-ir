[![Issues](https://img.shields.io/github/issues/janheinrichmerker/essir-medical-ir?style=flat-square)](https://github.com/janheinrichmerker/essir-medical-ir/issues)
[![Commit activity](https://img.shields.io/github/commit-activity/m/janheinrichmerker/essir-medical-ir?style=flat-square)](https://github.com/janheinrichmerker/essir-medical-ir/commits)
[![License](https://img.shields.io/github/license/janheinrichmerker/essir-medical-ir?style=flat-square)](LICENSE)

# ⚕️ essir-medical-ir

ESSIR 2023 hands-on for Medical IR.

## Resources

Thanks to the tutors for providing [many useful resources](https://github.com/ProjectDossier/essir-medical-session)!

## Installation

1. Install [Python 3.10](https://python.org/downloads/)
2. Create and activate virtual environment:
    ```shell
    python3.10 -m venv venv/
    source venv/bin/activate
    ```
3. Install dependencies:
    ```shell
    pip install -e .
    ```

## Testing

After [installing](#installation) all test dependencies (`pip install -e .[tests]`), you can run our approval tests:

```shell script
flake8 essir_medical_ir
pylint essir_medical_ir
bandit -c pyproject.toml -r essir_medical_ir
pytest essir_medical_ir
```

## License

This repository is licensed under the [MIT License](LICENSE).
