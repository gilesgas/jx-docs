---
date: 2018-09-17T16:50:47Z
title: "jx create addon sso"
slug: jx_create_addon_sso
url: /commands/jx_create_addon_sso/
---
## jx create addon sso

Create a SSO addon for Single Sign-On

### Synopsis

Creates the Single Sign-On addon 

This addon will install and configure the dex identity provider, sso-operator and cert-manager.

```
jx create addon sso [flags]
```

### Examples

```
  # Create the sso addon
  jx create addon sso
```

### Options

```
  -b, --batch-mode                In batch mode the command never prompts for user input
      --cluster                   Enable cluster wide Ingress upgrade
      --headless                  Enable headless operation if using browser automation
      --helm-update               Should we run helm update first to ensure we use the latest version (default true)
  -h, --help                      help for sso
      --install-dependencies      Should any required dependencies be installed automatically
  -n, --namespace string          The Namespace to install into (default "jx")
      --namespaces stringArray    Namespaces to upgrade
      --no-brew                   Disables the use of brew on MacOS to install or upgrade command line dependencies
  -r, --release string            The chart release name (default "jx")
  -s, --set string                The chart set values (can specify multiple or separate values with commas: key1=val1,key2=val2)
      --skip-auth-secrets-merge   Skips merging a local git auth yaml file with any pipeline secrets that are found
      --skip-certmanager          Skips certmanager installation
      --verbose                   Enable verbose logging
```

### SEE ALSO

* [jx create addon](/commands/jx_create_addon/)	 - Creates an addon

###### Auto generated by spf13/cobra on 17-Sep-2018
