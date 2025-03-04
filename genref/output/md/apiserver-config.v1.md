---
title: kube-apiserver Configuration (v1)
content_type: tool-reference
package: apiserver.config.k8s.io/v1
auto_generated: true
---
Package v1 is the v1 version of the API.

## Resource Types 


- [AdmissionConfiguration](#apiserver-config-k8s-io-v1-AdmissionConfiguration)
  
    


## `AdmissionConfiguration`     {#apiserver-config-k8s-io-v1-AdmissionConfiguration}
    




AdmissionConfiguration provides versioned configuration for admission controllers.

<table class="table">
<thead><tr><th width="30%">Field</th><th>Description</th></tr></thead>
<tbody>
    
<tr><td><code>apiVersion</code><br/>string</td><td><code>apiserver.config.k8s.io/v1</code></td></tr>
<tr><td><code>kind</code><br/>string</td><td><code>AdmissionConfiguration</code></td></tr>
    

  
  
<tr><td><code>plugins</code><br/>
<a href="#apiserver-config-k8s-io-v1-AdmissionPluginConfiguration"><code>[]AdmissionPluginConfiguration</code></a>
</td>
<td>
   Plugins allows specifying a configuration per admission control plugin.</td>
</tr>
    
  
</tbody>
</table>
    


## `AdmissionPluginConfiguration`     {#apiserver-config-k8s-io-v1-AdmissionPluginConfiguration}
    



**Appears in:**

- [AdmissionConfiguration](#apiserver-config-k8s-io-v1-AdmissionConfiguration)


AdmissionPluginConfiguration provides the configuration for a single plug-in.

<table class="table">
<thead><tr><th width="30%">Field</th><th>Description</th></tr></thead>
<tbody>
    

  
<tr><td><code>name</code> <B>[Required]</B><br/>
<code>string</code>
</td>
<td>
   Name is the name of the admission controller.
It must match the registered admission plugin name.</td>
</tr>
    
  
<tr><td><code>path</code><br/>
<code>string</code>
</td>
<td>
   Path is the path to a configuration file that contains the plugin's
configuration</td>
</tr>
    
  
<tr><td><code>configuration</code><br/>
<a href="https://godoc.org/k8s.io/apimachinery/pkg/runtime#Unknown"><code>k8s.io/apimachinery/pkg/runtime.Unknown</code></a>
</td>
<td>
   Configuration is an embedded configuration object to be used as the plugin's
configuration. If present, it will be used instead of the path to the configuration file.</td>
</tr>
    
  
</tbody>
</table>
    
  
