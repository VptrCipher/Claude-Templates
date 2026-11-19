---
name: write-tests
description: Use whenever you add or change code in this project. Write pytest tests and make sure they pass before finishing.
---
# Writing tests
- Put tests in tests/, named test_<module>.py.
- Cover the happy path, invalid input, and one edge case per endpoint.
- Run `pytest -q`. If anything fails, fix it and run again.
- Do not report the task as done until all tests pass.
