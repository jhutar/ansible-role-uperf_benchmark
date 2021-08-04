# ansible-role-uperf_benchmark

**Install and run uperf benchmark.**


## Installation

To install the role, create `requirements.yaml` with this content:

    - name: sosreport_gather
      src: https://github.com/jhutar/ansible-role-uperf_benchmark.git
      version: origin/main

and then to install the role:

    ansible-galaxy install -r requirements.yaml --roles-path roles/

Now the role is available in `roles/uperf_benchmark/`.

Check `uperf_benchmark.yaml` for example on how to use the role in the playbook.


## Configuration

* To do X you should set `uperf_benchmark_XYZ` variable


### Default variables

* `uperf_benchmark_XYZ` set to `ABC` by default


## References

1. To read more about sosreport
  - https://access.redhat.com/solutions/3592
