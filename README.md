# any VM Action

**The value for [runs-on](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idruns-on) should be set to either `macos-latest` or `ubuntu-latest` in order to have the best results with this action.**

This action allows the running of command-line programs via the `bash` shell of VMs provisioned with any VM using the [run](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idstepsrun) keyword. This also works with composite actions which exclusively use the `run` keyword (and/or call other composite actions which also do so.)

#### *This action is currently only tested with these os values (but will probably also work with others [see [here](https://github.com/anyvm-org/anyvm) for options]):*
  * `alpine`
  * `debian`
  * `freebsd`

# Usage
<!-- start usage -->
1. Provision a `VM` using the specified `os` (with 2 CPUs & 2GB of RAM)
    ```yaml
    - name: Provision VM
      uses: hummeltech/anyvm-action@v1
      with:
        os: alpine
        cpu: 2
        mem: 2048
    ```
2. Execute a command using the `run` keyword
    ```yaml
    - name: Display the contents of /etc/os-release
      run: cat /etc/os-release
    ```
<!-- end usage -->
