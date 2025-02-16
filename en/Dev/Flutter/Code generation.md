---
Planted: 2025-01-08
Tended: 2025-02-16
---
# Code Generation

*Planted: `= this.Planted`*
*Tended: `= this.Tended`*

---


Flutter is a boilerplate heavy framework, so a lot of code needs to be generated into separate files. To keep the project structured, the generated files can be placed in their own folders and more easily gitignored as well.
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