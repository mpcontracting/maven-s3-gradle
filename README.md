# maven-s3-gradle

## Usage

```
buildscript {
    dependencies {

    }
    repositories {
        mavenCentral()
    }
}

apply plugin: 'java'
apply from: 'http://maven-s3-gradle.s3-website-eu-west-1.amazonaws.com/build.gradle'

repositories {
    mavenCentral()

    mavenS3('s3://private-s3-bucket/release')
    mavenS3('s3://private-s3-bucket/snapshot')
}
```