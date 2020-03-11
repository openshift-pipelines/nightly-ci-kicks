# Nightly CI PR Kicks

This repository is what controls the OpenShift Pipelines CI

When you create a new PR against this repo it will get picked by the OpenShift-CI triggers and starts the nightly CI.

This will comment on your PR with a link to the openshift console to follow the build.

If you don't have access to the openshift console, you need to : 

1. Get access to the knative devint cluster https://github.com/openshift-knative/cluster-devint#github-team-membership
2. Request access from `chmouel` or `vincent` to issue this command : 
```
oc adm policy add-role-to-user admin ${KERBEROS_USERNAME} -n ci-openshift-pipelines
```

## Can I kick it ?

***Yes you can !!!***

![Yes you can](https://gifimage.net/wp-content/uploads/2018/06/yes-you-can-gif-4.gif)

Any PR would do it no need for fancy tags or other stuff to pick this up....

## Design diagrams

### CI worked flawlessly 

![Alt Text](https://media.giphy.com/media/3o6gE3pYgQLnFlyQfK/giphy.gif)

### CI is taking some time to pick up the change 

![Alt Text](https://i.pinimg.com/originals/cb/b4/a6/cbb4a65a2f45c0e068f817820ee6e720.gif)

### CI failed

![Alt Text](https://i.makeagif.com/media/2-22-2016/UCZp1c.gif)
