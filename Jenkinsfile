#!/usr/bin/env groovy

// Use container agents on odd numbered builds
// Assures that we test with container agents and without container agents
def useContainerForOddBuilds = ((BUILD_ID as int) % 2) as boolean

buildPlugin(
  useContainerAgent: useContainerForOddBuilds,
  configurations: [
    [platform: 'linux',   jdk: '17', jenkins: '2.346.3'],
    [platform: 'linux',   jdk: '11'],
    [platform: 'windows', jdk:  '8']
  ]
)
