# Enable Packman Repository on openSUSE Tumbleweed

After a fresh install of openSUSE Tumbleweed, some media content (such as videos in Firefox) may not play properly due to missing proprietary codecs. This is a common issue that can be resolved by enabling the **Packman** repository and switching the relevant packages to it.

This guide provides the necessary commands to enable Packman and perform a vendor switch to ensure proper multimedia support.

---

## 🛠 Steps to Fix Missing Media Codecs

Open a terminal and run the following commands:

```bash
# 1. Add the Packman repository with proper priority
sudo zypper ar -cfp 90 https://ftp.fau.de/packman/suse/openSUSE_Tumbleweed/ packman

# 2. Perform a full vendor switch to Packman for relevant packages
sudo zypper dup --from packman --allow-vendor-change
