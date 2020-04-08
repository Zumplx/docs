---
title: Device statuses
excerpt: Determine the status and connectivity of a device
---

# Device statuses

The application overview page shows the status of each device in the application.

<img src="/img/common/main_dashboard/application_device_status.png" alt="Application device status" width="40%" >

Each device can have one of the following statuses.

| Status            | Description                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------|
| Online            | The device is online and is connected to either the VPN or has recent API communications.    |
| Configuring       | The device is applying a configuration update.                                               |
| Updating          | The device is updating to a new application release.                                         |
| Offline           | The device is offline and is not connected to VPN and has not any recent API communications. |
| Post Provisioning | The device has been [provisioned][provisioned] but has not yet come online.                  |
| Inactive          | The device has been [deactivated][deactivated].                                              |

## Device connectivity

![Device connectivity indicators](/img/common/main_dashboard/device_status.png)

In addition to the device status, there are indicators to show if the device is currently connected to the VPN (checkmark icon) and has recent API communications (heartbeat icon). These indicators can be used to identify common issues, such as a firewall blocking VPN traffic or an inability of the device to reach the API endpoint.

For example, if the device is connected to the API only, indicated by a status of Online (Heartbeat Only), you may still see logs being sent and indicates that VPN traffic is blocked.

**Note:** If the device is powered off or loses all network connectivity, it will remain in the Online (Heartbeat Only) state for an extended time based on the device [API polling interval](https://www.balena.io/docs/learn/manage/configuration/#variable-list).

[provisioned]: /learn/welcome/primer/#device-provisioning
[deactivated]: /learn/manage/billing/#inactive-devices
[poll-interval]: /learn/manage/configuration/#variable-list
