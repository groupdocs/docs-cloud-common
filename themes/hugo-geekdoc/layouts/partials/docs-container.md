{{- $link := .Permalink -}}
{{- with .OutputFormats.Get "markdown" -}}
  {{- $link = .Permalink -}}
{{- end }}
{{ with .Site.GetPage .RelPermalink }} 
    {{- if .Params.index_title }}
##### [{{ .Params.index_title }}]({{ $link }}) 
    {{- else if .Params.breadcrumb }}
##### [{{ .Params.breadcrumb }}]({{ $link }}) 
    {{- else }}
##### [{{ .LinkTitle }}]({{ $link }}) 
    {{- end }} 
    {{ if .Params.last_updated }}
* **Last updated:** {{ .Params.last_updated }} 
    {{- end -}} 
    {{ if .Params.categories }}
* **Categories:** 
        {{- range .Params.categories }}
    * {{ . }} 
        {{- end -}} 
    {{- end -}} 
    {{ if .Params.tags }}
* **Tags:** 
        {{- range .Params.tags }} 
    * {{ . }} 
        {{- end -}} 
    {{- end -}} 
    {{ if .Params.brief }}

{{ .Params.brief }} 
    {{- end }} 
{{- end }}