# Helm Chart Deployment Using Ansible
**Prerequists**
1) AWS role to access these parameter store resources:
   * /jfrog/username
   * /jfrog/password 
2) aws policy to describe eks cluster "task-eks-cluster"
2) access on the kms key used by encrypt above parameters


## How Run playbook 
***Requirment:**

|   key         |  description                              |
| --------------|-------------------------------------------|     
| chart_name    |  name of chart needed to be deployed      |
| release_name  |  name of the release                      |
| version       |  chart version                            |
| namespace     |  namespace chart will be deployed to      |

 **Example:**
```bash
    ansible-playbook playbook.yaml -i  inventory -e chart_name=task -e release_name=task-service
    -e version=1.0.7 -e namespace=dev
```
