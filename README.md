[![release](https://img.shields.io/github/v/release/peribeir/homeassistant-rademacher)](https://github.com/peribeir/homeassistant-rademacher/releases/latest)
[![downloads](https://img.shields.io/github/downloads/peribeir/homeassistant-rademacher/total)](https://github.com/peribeir/homeassistant-rademacher/releases/latest)
[![issues](https://img.shields.io/github/issues/peribeir/homeassistant-rademacher)](https://github.com/peribeir/homeassistant-rademacher/issues)
[![hacs_badge](https://img.shields.io/badge/HACS-Default-41BDF5.svg)](https://github.com/hacs/integration)

![logo](https://github.com/peribeir/homeassistant-rademacher/raw/master/img/logo.png)
A Home Assistant custom Integration for local handling of Devices connected to Rademacher bridge.

### ATENTION: If using Home Pilot Gateway Premium, please delete and add Integration after upgrade to version 2.1.0

# Hardware Support (now with BETA support for HP Gateway Premium)

Works exclusively when devices are connected through HomePilot or Start2Smart Bridge.

**Bridges/Gateways from Rademacher are fully supported.**

***Version 2.x added BETA support for the new Homepilot Gateway Premium. Needs further testing.***

***HP Gateway Premium with local password protection not supported yet.***

### **Supports Covers, Switches, Sensors, Dimmers, Thermostats and Wall Controllers.**

*See full device list support at the end.*

### **Scenes are now supported since version 2.1.0** ###

Scenes will be automatically added as Home Assistant Scenes with "Homepilot" prefix. These scenes can be activated as any other Home Assistant Scene but cannot be edited.

# Installation

## 1. Using HACS (now on default repositories)

> HACS is a community store for integrations, Frontend extensions, etc. It makes installation and maintenance of this component much easier. You can find instructions on how to install HACS [here](https://hacs.xyz/).

Navigate to HACS in you Home Assistants Interface.

Click "Explore & Download Repositories"

Search for "Rademacher Homepilot Bridge"

Click "Download this Repository with HACS".

Select the version you wish do download and finally click "Download".

Restart Home Assistant.

## 2. Manually

Copy the `rademacher` folder into yout Home Assistant's `custom_components` folder.
This should be located under the `/config` folder.

If you haven't done it already, you should create the `custom_components` folder on your `/config`.

Restart Home Assistant.

# Usage

First of all, you should add the devices in you Home Pilot Application, or in the Bridge's Interface. The integration works by fetching the list that is registered in the Hub. 

## 1. Automatic Discovery

When Home Assistant Core is running on the same sub-network as the Hub,
if auto-discovery works, you'll see a notification on HA GUI stating it found new devices.

Just click "Check it Out" and you'll be presented with the Integrations page where you should see the new Rademacher Bridge entry.

Click "Configure". If you have set a password for the Hub, enter it and press "Submit".

On the next dialog, Choose any device that you may want to exclude from managing in HA. If you want to manage all, just press "Submit".

You should now be presented with Device/Entities detected, you should select the HA Area where you want to add them.

## 2. Using Config Flow

If Hub has not been auto-discovered, or you just deleted the integration and want to add again:

Start by going to Configuration > Integrations, then press the "Add Integration" button.

Then, search for Rademacher and select it.

In the Dialog that appears, insert the HostName/IP Address of the Rademacher Bridge. Ex: `bridge.local` or `192.168.1.60`

Press "Submit".

If you have configured a password for the hub, you'll be asked for it. Just insert it and press "Submit".

On the next dialog, Choose any device that you may want to exclude from managing in HA. If you want to manage all, just press "Submit".

You should now be presented with Device/Entities detected, you should select the HA Area where you want to add them.

# Direct and Indirect Contributors

<!-- readme: contributors,thmnxo4,MrWeidenMr,fritte87 -start -->
<table>
<tr>
    <td align="center">
        <a href="https://github.com/peribeir">
            <img src="https://avatars.githubusercontent.com/u/7266291?v=4" width="100;" alt="peribeir"/>
            <br />
            <sub><b>Pedro Ribeiro</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/michelde">
            <img src="https://avatars.githubusercontent.com/u/10096708?v=4" width="100;" alt="michelde"/>
            <br />
            <sub><b>Michel Munzert</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/duhow">
            <img src="https://avatars.githubusercontent.com/u/1145001?v=4" width="100;" alt="duhow"/>
            <br />
            <sub><b>David Girón</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/misa1515">
            <img src="https://avatars.githubusercontent.com/u/61636045?v=4" width="100;" alt="misa1515"/>
            <br />
            <sub><b>Misa1515</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/der-berni">
            <img src="https://avatars.githubusercontent.com/u/5528912?v=4" width="100;" alt="mrweidenmr"/>
            <br />
            <sub><b>der-berni</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/thmnxo4">
            <img src="https://avatars.githubusercontent.com/u/76701693?v=4" width="100;" alt="thmnxo4"/>
            <br />
            <sub><b>Thmnxo4</b></sub>
        </a>
    </td>
  </tr>
  <tr>
    <td align="center">
        <a href="https://github.com/mrweidenmr">
            <img src="https://avatars.githubusercontent.com/u/99197872?v=4" width="100;" alt="mrweidenmr"/>
            <br />
            <sub><b>Mrweidenmr</b></sub>
        </a>
    </td></tr>
</table>
<!-- readme: contributors,thmnxo4,MrWeidenMr -end -->

# Supported Devices
[List](https://github.com/Uvve-Dev/homeassistant-rademacher/wiki/Supported-Devices)
