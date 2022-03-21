# gitops-config-template

An opinionated gitops structure

- Mono repo
- Single branch i.e. main and then separate folders per environment
- ArgoCD for application deployment
- Helm for templatization

## Hierarchy

Tenant (Product) owns Applications which are promoted to different Environments (Static and Dynamic)

Tenant >> Applications >> Environments

This gitops structure supports:

- Multiple tenants/teams/products
- Multiple environments (both static and dynamic)
- Multiple clusters
- Multiple apps

## Mutliple tenants

We have 2 product based tenants:

- gabbar
- veeru

Who have exactly same structure

And then there is one special tenant which is SRE

## Mutliple environments

We have 5 environments for each application:

- build
- preview
- dev
- stage
- prod

## Multiple clusters

We have 2 clusters:

- Cluster # 1 holds: build, preview and dev
- Cluster # 2 holds: stage and prod

## Multiple apps

We have 3 apps:

- gabbar has two apps: stakater-nordmart-review, stakater-nordmart-review-ui
- veeru has one app: stakater-nordmart-inventory

## CI/CD/CD Workflow

[CI/CD/CD Source](https://www.websequencediagrams.com/?lz=dGl0bGUgQ29udGludW91cyBJbnRlZ3JhdGlvbgoKcGFydGljaXBhbnQgRGV2ZWxvcGVyAAkNQ29kZSBSZXBvAB8NVGVrdG9uADINSW1hZ2UgUmVnaXN0cnkATQ1LOHMgRGV2AGENQXJ0aWZhY3RvAB0PR2l0T3BzAGASQXJnAHUOSzhzIFFBCgoAgS4JLT4AgSMJOiBnaXQgcHVzaAoAgTcJLT4AgS8GOiB3ZWJob29rCm5vdGUgcmlnaHQgb2YAgUwHOiBzZXR1cAoAgVsGAEATbGwAIRducG0gdGVzdAAEG3J1biBidWlsZFxuAAIFIGltYWdlAGMJAII0DjoAgTsFABwHAIEVFmRlcGxveVxuaGVsbSB0ZW1wbGF0ZS4uLgCBNQkAgnIHOiBvYyBhcHBseSAtZgoAgwcHAFwUAIFMEQA4CXJ1bgBuHWhlYWx0aABnEkdFVCAvABYHAIJaFnRhZy1yZWxlYXMAggAKAIM-C2FkZCB0YWcAgxYXaW0AMwoAgQEYbG0ATxEAhHILOiBwdWJsaXNoACUFIGNoYXIAgysYZ2l0b3BzAIQSCQCFHws6IHVwZGF0ZSBRQSBmb2xkZXIKQXJnbwAVDwCEOAkAFgYAhTsGOiBzeW5jCg&s=default#)

![CI/CD/CD](./docs/images/ci-cd-cd-v1.png)