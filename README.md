# ansible-role-uperf_benchmark

**Install and run uperf benchmark.**


## Installation

To install the role, create `requirements.yaml` with this content:

    - name: uperf_benchmark
      src: https://github.com/jhutar/ansible-role-uperf_benchmark.git
      version: origin/main

and then to install the role:

    ansible-galaxy install -r requirements.yaml --roles-path roles/

Now the role is available in `roles/uperf_benchmark/`.

Check `uperf_benchmark.yaml` for example on how to use the role in the playbook.


## Configuration

* `uperf_benchmark_store_local_logs_dir` - if set, download raw logs from uperf to that local Ansible controller host directory. If empty, do not download the logs
* `uperf_benchmark_host_active` and `uperf_benchmark_host_passive` - two nodes (running `uperf -m` and `uperf -s`) used to run the tests, currently only 1 and 1 hosts are allowed there
* `uperf_benchmark_profile` - uperf profile
* `uperf_benchmark_param_*` - uperf profile parameters, currently only `proto`, `nthr` and `iter` are supported

### Default variables

```
# By default, do not collect logs
uperf_benchmark_store_local_logs_dir: ''

# Hosts to run on
uperf_benchmark_host_active: foo.example.com
uperf_benchmark_host_passive: passive.example.com

# Profile
uperf_benchmark_profile: /usr/share/uperf/iperf.xml
uperf_benchmark_param_proto: tcp
uperf_benchmark_param_nthr: 1
uperf_benchmark_param_iter: N/A
```


## References

1. To read more about uperf: http://uperf.org/manual.html
