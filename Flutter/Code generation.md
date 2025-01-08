#### Place generated code in sub-folders:

`build.yaml`
```yaml
targets:
  $default:
    builders:
      source_gen:combining_builder:
        options:
          build_extensions:
            'lib/{{dir}}/{{file}}.dart': 'lib/{{dir}}/.generated/{{file}}.g.dart'
      nameof|nameof:
	    enabled: true
        options:
          build_extensions:
            'lib/{{dir}}/{{file}}.dart': 'lib/{{dir}}/.generated/{{file}}.nameof.dart'
```

Each script using generated code should include:
`part '.generated/[script name].[x].dart';`