# Alternative way to merge multiple Butane files

This repo contains a script to merge multiple [Butane](https://github.com/coreos/butane) files, validate the result and finally transpile it to [Ignition](https://github.com/coreos/ignition).  
It solves head-aches of those who decided to follow best practices and split their growing Flatcar OS configuration into multiple files.

Inspired by [official docs](https://www.flatcar.org/docs/latest/learning-series/advanced-service-config/#splitting-the-configuration-file) of Flatcar.  
The included example is based on the same docs.

Usage:
- download the `merge_validate_transpile.sh` script and make it executable (`chmod +x merge_validate_transpile.sh`)
- edit it (set `input_files` variable value to list all your Butane files)
- run it (`.\merge_validate_transpile.sh`)
- in case of errors - fix them and repeat the previous step
- use the resulting `result_ignition.ign` to configure your Flatcar OS instance

How to run tests:
- make sure the `input_files` variable has its default value (i.e. points to example files in this repo)
- uncomment one of test cases in `input_tests.yaml` file (make sure only one test is uncommented at a time)
- run the main script (`.\merge_validate_transpile.sh`)
- compare the actual and expected results
- repeat for other test cases

Kudos to:
- Mike Farah
- Flatcar
- Docker
