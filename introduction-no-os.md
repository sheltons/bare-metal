---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# The no OS option
{: #bm-no-os}

No OS is an option to order a bare metal server without an operating system.

## How to order a bare metal server with no OS?

Start by placing an order for a bare metal server via [{{site.data.keyword.Bluemix}} console ![External link icon](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window}.

1. Select **Other** from **System Configuration > Operating System**.
2. Select **No Operating System**.

## How to install an operating system on a no OS server?

There are two methods to install an operating system on a bare metal server with no operating system.

### Option 1: PXE Server

A bare metal server with no operating system can be set up to boot and load the OS from a PXE setup.<!--(see [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) for more information)--> Deploy the bare metal server in a network environment with a PXE setup (this usually involves running a DHCP and TFTP daemon) and configure the new bare metal server BIOS to boot from the network adapter. For the no OS option to work properly, PXE setup needs to be in the same VLAN as the bare metal server, or DHCP forwarding needs to be used.

**Note:** It might be necessary to open a support ticket to request that the switch ports be regrouped in basic mode for this option to work. This is because the PXE protocol does not require compatibility with link aggregation (LACP), <!--see [Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation))--> which is now a standard capability to provide redundancy. Another option is to order the server with Unbonded uplinks (no link aggregation) and then change them to redundant uplinks after the OS is installed.

### Option 2: IPMI device

Install an operating system on to a bare metal server with no operating system by booting from an ISO via the included IPMI device. For more information about booting from an ISO, see [Mounting an ISO on a bare metal server](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server).
