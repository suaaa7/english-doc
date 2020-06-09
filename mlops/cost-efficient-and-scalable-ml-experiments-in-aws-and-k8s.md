# Cost-efficient and scalable ML-experiments in AWS with spot-instances, Kubernetes and Horovod

http://blog.rosebud.ai/cost-efficient-and-scalable-model-training-in-aws/amp/

https://speakerdeck.com/keigohtr/cost-efficient-and-scalable-ml-experiments-in-aws-with-spot-instances-kubernetes-and-horovod-falseshao-jie-togan-xiang

## Summary

- In this article you will see how with minimal changes to our ML-code we:
    - provision spot compute-resources using AWS's EKS,
    - represent ML-experiments as Kubernetes jobs,
    - manage weights and experiment-summaries, and
    - perform single-machine distributed training on multiple GPUs.

- Storage in the Cloud
- Spot Instances: Cheap Compute
- Managing Compute-Resources with EKS and Kubernetes
- One-time setup
- Defining Compute-Tasks
- Code Modifications
- Single-machine multi-GPU distributed training
- Final Thoughts

## Note

- Storage in the Cloud
    - S3
    - EFS
    - EBS

### Technical terms

### Important sentences

Lastly, if using randomization when splitting dataset into test and training sets, the random-seed must be fixed. This will ensure that split is identical between experiment's restarts and also across distributed workers.

integrate Kubernetes Job-manifests with hyperparameter-tuning libraries, so that experiments can be automatically created and scheduled on the cluster.
=> k8s + optuna

### Sentences I couldn't understand

### Word etc

cutting-edge: 最前線、最先端
outline: 概要、あらまし、概説する、概要を説明する
spotty: まだらな、むらのある
repurpose: 別の目的のための再利用する
in a nutshell: かいつまんで、簡単に言えば
parity: 同質であること、等価、同等、同格
bundle: 包み、固まり、包む
loose: 自由な、放たれた、解き放つ、自由にする
negate: 否定する、打ち消す、無効にする
