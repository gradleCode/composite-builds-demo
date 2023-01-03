# 项目结构

```shell
├── services
│   ├── service1
│   │   ├── build.gradle
│   │   └── settings.gradle
│   └── service2
│       ├── build.gradle
│       └── settings.gradle
├── settings.gradle
└── shared
    ├── lib1
    │   ├── build.gradle
    │   └── settings.gradle
    └── lib2
        ├── build.gradle
        └── settings.gradle
```

# 执行测试

```shell
./gradlew :lib1:clean :lib2:clean :service1:clean :service1:build --console=verbose
```

```shell
> Task :lib2:clean
> Task :service1:clean
> Task :lib1:clean
> Task :service1:processResources NO-SOURCE
> Task :lib2:compileJava NO-SOURCE
> Task :lib1:compileJava NO-SOURCE
> Task :service1:processTestResources NO-SOURCE
> Task :lib2:processResources NO-SOURCE
> Task :lib1:processResources NO-SOURCE
> Task :lib2:classes UP-TO-DATE
> Task :lib1:classes UP-TO-DATE
> Task :lib2:jar
> Task :lib1:jar
> Task :service1:compileJava NO-SOURCE
> Task :service1:classes UP-TO-DATE
> Task :service1:jar
> Task :service1:assemble
> Task :service1:compileTestJava NO-SOURCE
> Task :service1:testClasses UP-TO-DATE
> Task :service1:test NO-SOURCE
> Task :service1:check UP-TO-DATE
> Task :service1:build
```