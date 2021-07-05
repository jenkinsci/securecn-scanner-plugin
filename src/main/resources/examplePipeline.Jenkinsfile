pipeline {
    agent any
    stages{
        stage ('secureCN') {
            steps {
                secureCNVulnerabilityScanner(imageName: 'registry.gitlab.com/portshift/portshift/base:v1',
                  secureCnAccessKey: 'f5486ec2-7ba2-4e37-8aed-de700294bc76', secureCnSecretKeyId: 'secureCnSecretKey',
                  highestSeverityAllowed: 'HIGH', dockerRegistryPasswordId: 'benGitlab',
                  highestSeverityAllowedDf: 'FATAL', url: 'securecn.cisco.com')
            }

        }
    }
}