<h1 align="center">Hestia Control Panel - Compiled Releases</h1>

LINK TO OFFICIAL HESTIA CONTROL PANEL: https://github.com/hestiacp/hestiacp

Because Hestia Control Panel uses implements a "rolling release" framework and doesn't maintain full, compiled, installable releases of past versions of their panel, per their instructions, from time to time, I compile their releases using the instructions here: 

https://hestiacp.com/docs/contributing/building.html#installing-hestia-from-a-branch 

with the note about how to compile a specific version here: 

https://forum.hestiacp.com/t/what-is-the-correct-way-to-install-specific-hestia-release-version/12837/17 

and post them here for my own install purposes to achieve production system stablity.

## IMPORTANT SECURITY NOTE

- Hestia does not release security patches for previous versions. You must upgrade to the latest version for the latest security patches. Their general recommendation is to keep hestia updated to the latest version via their auto-update system.
- THE COMPILED FILES IN THIS REPOSITORY HAVE NOT BEEN MODIFIED IN ANY WAY. However, there is no way (that I know of) to checksum the compiled tar against anything. If you doubt this repository, you can always use the instructions above to compile for yourself.

## INSTALL

**DOWNLOAD/EXTRACT:**
- It is recommended you extract the `.tar.gz` to `/tmp`
- The `.tar.gz` will extract to subdirectory `./hestiacp-src`
- `/tmp/hestiacp-src` is the same static output directory of the complier.
- ** CHANGE THE VERSION NUMBER BELOW IN THREE PLACES. **

```bash
cd /tmp && wget https://github.com/ev0net/hestiacp-compiled-releases/releases/download/1.8.11/hestiacp-src-1.8.11.tar.gz && tar -xzvf hestiacp-src-1.8.11.tar.gz
```

**RUN INSTALLER:** 
- OS OPTIONS: `hst-install-ubuntu.sh` || `hst-install-debian.sh`
- Do not run `hst-install.sh` as it will pull latest `hst-install-[os}.sh` and may cause problems.
- If needed, add other install options: https://hestiacp.com/docs/introduction/getting-started.html#list-of-installation-options

```bash
cd /tmp && cp /tmp/hestiacp-src/hestiacp-localsrc/install/hst-install-ubuntu.sh . && bash hst-install-ubuntu.sh --with-debs /tmp/hestiacp-src/deb/
```
