---
layout: mod

authors: "juso" # Authors of the mod
title: ConfigurableViewModel (CVM) # Title of the mod
version: "1.0" # Version of the mod
supported: "BL2 + TPS" # Supported games; currently can only display as "BL2", "BL2 + TPS", or "TPS"

tagline: "Allows you to easily change the ViewModel for each WeaponType with ingame sliders." # A short description of the mod itself.
description: "Allows you to easily change the ViewModel for each WeaponType with ingame sliders." # This is set in order to keep the SEO proper
longDescription: "A mod that allows you to change the viewmodel of any WeaponType.\nTo change your viewmodel go ingame,\n ``Escape``-&gt;``Mods``-&gt;``CVM``![yt](https://www.youtube.com/watch?v=nABmVIYpuXg)" # Description of what the mod can do
categories: ['Utility'] # Category of the type of mod

requirements: [] # Requirements for the given mod
requirementTitles: [] # The link-friendly name of the requirements

issues: ""
download: "https://raw.githubusercontent.com/juso40/bl2sdk_Mods/master/ConfigurableViewmodel/__init__.py"
license: ['MIT', 'https://choosealicense.com/licenses/mit'] # License name, link about the license from https://choosealicense.com/

---
**Contents**
* TOC
{:toc}

## {{page.title}}

Mod by: {{page.authors}}
Current Version: {{page.version}}

<p></p>
### Description

{{page.longDescription | markdownify }}

Currently Supports: `{{page.supported}}`

{% if page.categories.size > 0 %}
Categories:
{% for category in page.categories %}
  * [{{category}}](/types/{{category}})
{% endfor %}
<p></p>
{% endif %}

{% if page.requirements.size > 0 %}
### Requirements

{% for requirement in page.requirements %}

{% assign reqName = page.requirementTitles[forloop.index0] %}

{% for mod in site.mods %}

{% assign modName = mod.path | remove_first: '_mods/' %}
{% assign xz = reqName | append: '.md' %}

{% if modName == xz %}
* [{{ requirement }}]( {{ reqName | relative_url | prepend: '/mods'}} ) <sup>[(Direct Download)]({{mod.download}})</sup>
{% endif %}
{% endfor %}

{% endfor %}
<p></p>
{% endif %}

### Links

{% if page.download != "" %}
You can download {{page.title}} here: [Download Link]({{page.download}})
{% endif %}

{% if page.issues != "" %}
Report issues here: [{{page.issues}}]({{page.issues}})
{% endif %}

{% if page.license.size > 0 %}
This mod is licensed using {{page.license[0]}} <sup>[?]({{page.license[1]}})
{% endif %}