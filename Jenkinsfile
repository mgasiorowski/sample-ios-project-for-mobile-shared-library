#!groovy
@Library('jenkins-mobile-pipeline-shared-libraries') _

pipelineOptions {
    maxNumberBuildsToKeep = 10
}

synchronizeBuildNumbers {
    platformName = 'ios'
    projectName = 'mobile_shared_library'
}

checkoutScm {
    nodeLabel = 'mac_mini_wp'
}

iosStaticAnalysis {
    nodeLabel = 'mac_mini_wp'
    fastlaneLane = 'analyze'
}

iosSwiftlint {
    nodeLabel = 'mac_mini_wp'
    fastlaneLane = 'swiftlint'
}

iosTests {
    stageSuffix = 'Unit'
    nodeLabel = 'mac_mini_wp'
    fastlaneLane = 'unit_tests'
}


iosBuild {
    stageSuffix = 'Build'
    nodeLabel = 'mac_mini_wp'
    fastlaneLane = 'build'
}
