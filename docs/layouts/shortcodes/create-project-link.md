<!-- Link to create projects.
  For a specific template, call with `template="<FRAMEWORK>"`.
  For just templates in general, call with `template=true`.
  We prefer putting people on the template search page to opening a specific template
  because they get more context that way.

  To link to create a new project from scratch, call with `scratch=true`.

  This all is on one line so that it can be added within Markdown.
  Example: [Link text](\{\{ create-project-link template=true }})
  Without the backslashes.
  -->
https://console.platform.sh/org/create-project{{ $suffix := printf "?" }}{{ with .Get "scratch" }}{{ $suffix = "/info?" }}{{ end }}{{ with .Get "template" }}{{ $suffix = "/template?" }}{{ if eq (printf "%T" .) "string" }}{{ $suffix = printf "%squery=%s&" $suffix . }}{{ end }}{{ end }}{{ $suffix }}_utm_campaign=cta_deploy_marketplace_template&utm_source=public_documentation&_utm_medium=organic
