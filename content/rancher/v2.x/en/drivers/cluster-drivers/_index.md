---
title: Cluster Drivers
weight: 1
aliases:
---
_Available as of v2.2_

Cluster drivers are used to create clusters in a [hosted Kubernetes provider]({{< baseurl >}}/rancher/v2.x/en/cluster-provisioning/hosted-kubernetes-clusters/), such as Google GKE.

A cluster driver is similar to a node driver but for provisioning *hosted* kubernetes clusters for different cloud providers. Rancher uses the provider's API to provision and manage the cluster. The availability of which cluster driver to display when creating clusters is defined by the cluster driver's status. Only `active` cluster drivers will be displayed as an option for creating clusters. By default, Rancher is packaged with several existing cloud provider cluster drivers but you can also add custom cluster drivers to Rancher.

If there are specific cluster drivers that you do not want to show your users, you may deactivate those cluster drivers within Rancher and they will not appear as an option for cluster creation.

### Managing Cluster Drivers
>**Prerequisites:** To create, edit, or delete drivers, you need _one_ of the following permissions:
>
>- [Administrator Global Permissions]({{< baseurl >}}/rancher/v2.x/en/admin-settings/rbac/global-permissions/)
>- [Custom Global Permissions]({{< baseurl >}}/rancher/v2.x/en/admin-settings/rbac/global-permissions/#custom-global-permissions) with the [Manage Cluster Drivers]({{< baseurl >}}/rancher/v2.x/en/admin-settings/rbac/global-permissions/#global-permissions-reference) role assigned.

## Activating/Deactivating Cluster Drivers

By default, Rancher only activates drivers for the most popular cloud providers, Amazon EC2, Azure, DigitalOcean and vSphere. If you want to show or hide any node driver, you can change it's status.

1.	From the **Global** view, select **Drivers** from the main menu.

2.  From the **Drivers** page, select the **Cluster Drivers** tab.

3. Select the driver that you wish to **Activate** or **Deactivate** and select the appropriate icon ![icon]({{< baseurl >}}/img/rancher/drivers/activate_deactivate.png).



## Adding Custom Cluster Drivers

If you want to use a cluster driver that Rancher doesn't support out-of-the-box, you can add the provider's driver in order to start using them to create _hosted_ kubernetes clusters. 

1. From the **Global** view, select **Drivers** from the main menu.

2. From the **Drivers** page select the **Cluster Drivers** tab

3. Click **Add Cluster Driver**.

4. Complete the **Add Cluster Driver** form. Then click **Create**

To develop your own pluggable cluster UI driver please see this [example](https://github.com/rancher-plugins/kontainer-engine-driver-example)