This is a collection of container images used for running tests in build pipelines and are built and stored in this projects' GitLab instance and container registry

You can use containers from this project by referencing container images in this registry in other project pipelines like

```yml
# assuming a test container named selenium-jdk:17.0.2
integration tests:
  stage: test-integration
  image: registry.gitlab.com/test-containers/selenium-openjdk:17.0.2
  script:
    - cd some/test/directory
    - ./gradlew test
```
