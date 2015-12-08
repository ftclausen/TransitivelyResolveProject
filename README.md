Small project to demonstrate how you can't have a configuration called `install`
on a rootProject build.gradle using the block definition e.g. **this breaks**

    configurations {
        install
    }

    dependencies {
        install 'com.example:widgetMaker:1.0.0'
    }

it only works if you use

    configurations.create('install')

