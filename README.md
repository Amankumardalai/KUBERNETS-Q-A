# KUBERNETS QUESTIONS
What is a Kubernetes Deployment, and why is it used?

A Kubernetes Deployment is like a blueprint for your application. It's used to make sure your application runs smoothly, and if something goes wrong, it fixes it automatically.
Explain the key difference between a Deployment and a Pod.

A Pod is like a single instance of your application, while a Deployment manages many Pods. Deployments make sure you have the right number of Pods running and healthy.
How does a Deployment ensure the desired number of Pods are running and healthy?

A Deployment keeps an eye on your Pods. If it sees too few or unhealthy Pods, it creates new ones to replace them, making sure you always have the right number.
What are rolling updates and rollbacks in the context of Deployments?

Rolling updates are a way to change your application without stopping it. Rollbacks are like an "undo" button if something goes wrong during an update.
Can you describe the purpose of the 'strategy' field in a Deployment specification?

The 'strategy' field tells Kubernetes how to do updates. It can be set to 'Recreate' (replace all Pods at once) or 'RollingUpdate' (replace them gradually).
What is the significance of the 'maxSurge' and 'maxUnavailable' fields during rolling updates?

'maxSurge' says how many new Pods can be created during an update, and 'maxUnavailable' says how many old Pods can be removed. It controls the update speed.
How can you scale a Deployment horizontally to increase the number of replicas?

To scale a Deployment, you change the 'replica' number in the Deployment's configuration. This tells Kubernetes how many replicas (copies) of your app to run.
What is a rolling deployment, and how does it work?

A rolling deployment updates your app gradually, one Pod at a time. It replaces old Pods with new ones, so your app stays available during updates.
Explain the use of 'kubectl rollout' commands in managing Deployments.

'kubectl rollout' commands help you manage Deployments. You can use them to start, pause, resume, or check the status of an update.
What happens when a Deployment encounters a Pod that is in a 'Pending' or 'Failed' state during an update?

If a Pod is 'Pending' or 'Failed' during an update, the Deployment waits and keeps the old version running until the new version is ready.
How can you pause and resume a Deployment rollout?

You can pause a Deployment rollout with 'kubectl rollout pause' and resume it with 'kubectl rollout resume' when you're ready to continue.
What are the benefits of using Deployments for application management compared to directly managing Pods?

Using Deployments makes life easier. They handle scaling, updates, and rollbacks automatically. It's like having a helpful assistant managing your app, so you don't have to do everything manually. This reduces mistakes and makes your app more reliable.
