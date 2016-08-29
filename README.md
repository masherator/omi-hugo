# OMI Oriental Grocery Website

This is a small project to help me learn about Hugo, Git and GitHub.

## Menu 

The Following Code block was used for menu creation but we are currently using the [Lazy Blogger Implementation](https://gohugo.io/extras/menus/) which keys off the config.

~~~~

{{ $currentNode := . }}
{{ range .Site.Menus.main }}
<li>
    {{ if or ($currentNode.IsMenuCurrent "main" .) ($currentNode.HasMenuCurrent "main" .) }}
    <a href="{{ .URL }}" class="current">{{ .Name }}</a>
    {{ else }}
    <a href="{{ .URL }}">{{ .Name }}</a>
    {{ end }}
</li>
{{ end }}

~~~~