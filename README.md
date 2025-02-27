# cfn-modules: Fargate service

Fargate service.

> :books: Check out our new book [Rapid Docker on AWS](https://cloudonaut.io/rapid-docker-on-aws/?utm_source=cfn-modules&utm_medium=doc&utm_campaign=fargate-service)
> * Written for DevOps engineers and web developers who want to run dockerized web applications on AWS.
> * Prior knowledge of Docker and AWS is not required.
> * Continuous Deployment of your Web Application and Infrastructure as Code.

## Install

> Install [Node.js and npm](https://nodejs.org/) first!

```
npm i @cfn-modules/fargate-service
```

## Usage

```
---
AWSTemplateFormatVersion: '2010-09-09'
Description: 'cfn-modules example'
Resources:
  Service:
    Type: 'AWS::CloudFormation::Stack'
    Properties:
      Parameters:
        VpcModule: !GetAtt 'Vpc.Outputs.StackName' # required
        ClusterModule: !GetAtt 'Cluster.Outputs.StackName' # optional
        TargetModule: '' # optional
        FileSystemModule1: '' # optional
        AlertingModule: '' # optional
        ClientSgModule1: '' # optional
        ClientSgModule2: '' # optional
        ClientSgModule3: '' # optional
        ManagedPolicyArns: '' # optional
        ProxyImage: '' # optional
        ProxyImageSecretModule '' # optional
        ProxyPort: '8000' # optional
        ProxyEnvironment1Key: '' # optional
        ProxyEnvironment1Value: '' # optional
        ProxyEnvironment1SecretModule: '' # optional
        ProxyEnvironment2Key: '' # optional
        ProxyEnvironment2Value: '' # optional
        ProxyEnvironment2SecretModule: '' # optional
        ProxyEnvironment3Key: '' # optional
        ProxyEnvironment3Value: '' # optional
        ProxyEnvironment3SecretModule: '' # optional
        ProxyEnvironment4Key: '' # optional
        ProxyEnvironment4Value: '' # optional
        ProxyEnvironment4SecretModule: '' # optional
        ProxyEnvironment5Key: '' # optional
        ProxyEnvironment5Value: '' # optional
        ProxyEnvironment5SecretModule: '' # optional
        AppImage: 'widdix/hello:v1' # optional
        AppImageSecretModule '' # optional
        AppPort: '80' # optional
        AppEnvironment1Key: '' # optional
        AppEnvironment1Value: '' # optional
        AppEnvironment1SecretModule: '' # optional
        AppEnvironment2Key: '' # optional
        AppEnvironment2Value: '' # optional
        AppEnvironment2SecretModule: '' # optional
        AppEnvironment3Key: '' # optional
        AppEnvironment3Value: '' # optional
        AppEnvironment3SecretModule: '' # optional
        AppEnvironment4Key: '' # optional
        AppEnvironment4Value: '' # optional
        AppEnvironment4SecretModule: '' # optional
        AppEnvironment5Key: '' # optional
        AppEnvironment5Value: '' # optional
        AppEnvironment5SecretModule: '' # optional
        AppEnvironment6Key: '' # optional
        AppEnvironment6Value: '' # optional
        AppEnvironment7Key: '' # optional
        AppEnvironment7Value: '' # optional
        AppEnvironment8Key: '' # optional
        AppEnvironment8Value: '' # optional
        AppEnvironment9Key: '' # optional
        AppEnvironment9Value: '' # optional
        AppEnvironment10Key: '' # optional
        AppEnvironment10Value: '' # optional
        AppEnvironment10Key: '' # optional
        AppEnvironment10Value: '' # optional
        AppEnvironment11Key: '' # optional
        AppEnvironment11Value: '' # optional
        AppEnvironment12Key: '' # optional
        AppEnvironment12Value: '' # optional
        AppEnvironment13Key: '' # optional
        AppEnvironment13Value: '' # optional
        AppEnvironment14Key: '' # optional
        AppEnvironment14Value: '' # optional
        AppEnvironment15Key: '' # optional
        AppEnvironment15Value: '' # optional
        AppEnvironment16Key: '' # optional
        AppEnvironment16Value: '' # optional
        AppEnvironment17Key: '' # optional
        AppEnvironment17Value: '' # optional
        AppEnvironment18Key: '' # optional
        AppEnvironment18Value: '' # optional
        AppEnvironment19Key: '' # optional
        AppEnvironment19Value: '' # optional
        AppEnvironment20Key: '' # optional
        AppEnvironment20Value: '' # optional
        SidecarImage: '' # optional
        SidecarImageSecretModule '' # optional
        SidecarPort: '9000' # optional
        SidecarProtocol: 'tcp' # optional
        SidecarEnvironment1Key: '' # optional
        SidecarEnvironment1Value: '' # optional
        SidecarEnvironment1SecretModule: '' # optional
        SidecarEnvironment2Key: '' # optional
        SidecarEnvironment2Value: '' # optional
        SidecarEnvironment2SecretModule: '' # optional
        SidecarEnvironment3Key: '' # optional
        SidecarEnvironment3Value: '' # optional
        SidecarEnvironment3SecretModule: '' # optional
        SidecarEnvironment4Key: '' # optional
        SidecarEnvironment4Value: '' # optional
        SidecarEnvironment4SecretModule: '' # optional
        SidecarEnvironment5Key: '' # optional
        SidecarEnvironment5Value: '' # optional
        SidecarEnvironment5SecretModule: '' # optional
        Cpu: '0.25' # optional
        Memory: '0.5' # optional
        DesiredCount: '2' # optional
        MaxCapacity: '4' # optional
        MinCapacity: '2' # optional
        LogsRetentionInDays: '14' # optional
        SubnetsReach: 'Public' # optional
        AutoScaling: 'true' # optional
        HealthCheckGracePeriodSeconds: '60' # optional
        Spot: 'false' # optional
        CpuArchitecture: 'X86_64' # optional
        OperatingSystemFamily: 'LINUX' # optional
        ExecuteCommand: 'false' # optional
      TemplateURL: './node_modules/@cfn-modules/fargate-service/module.yml'
```

## Examples

* [fargate-alb-proxy-pattern](https://github.com/cfn-modules/docs/tree/master/examples/fargate-alb-proxy-pattern)
* [fargate-alb-single-container](https://github.com/cfn-modules/docs/tree/master/examples/fargate-alb-single-container)

## Related modules

* [alb](https://github.com/cfn-modules/alb)
* [nlb](https://github.com/cfn-modules/nlb)

## Parameters

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Default</th>
      <th>Required?</th>
      <th>Allowed values</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>VpcModule</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/vpc">vpc module</a></td>
      <td></td>
      <td>yes</td>
      <td></td>
    </tr>
    <tr>
      <td>ClusterModule</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/ecs-cluster">ecs-cluster module</a> (if empty, an ECS cluster is created)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>TargetModule</td>
      <td>Stack name of <a href="https://www.npmjs.com/search?q=keywords:cfn-modules:Target">module implementing Target</a></td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>FileSystemModule1</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/efs-file-system">efs-file-system module</a> mounted to /mnt/efs1</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AlertingModule</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/alerting">alerting module</a></td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ClientSgModule1</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/client-sg">client-sg module</a> to mark traffic from Fargate task</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ClientSgModule2</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/client-sg">client-sg module</a> to mark traffic from Fargate task</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ClientSgModule3</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/client-sg">client-sg module</a> to mark traffic from Fargate task</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ManagedPolicyArns</td>
      <td>Comma-delimited list of IAM managed policy ARNs to attach to the task's IAM role</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyImage</td>
      <td>Docker image to use for the proxy container. You can use images in the Docker Hub registry or specify other repositories (repository-url/image:tag). If the repository is private, set ProxyyImageSecretModule as well!</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyImageSecretModule</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> which contains the repository credentials for private registry authentication</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyPort</td>
      <td>The port exposed by the proxy container that receives traffic from the load balancer (ProxyPort != AppPort != SidecarPort; ignored if ProxyImage and/or TargetModule are/is not set)</td>
      <td>8000</td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment1Key</td>
      <td>Environment variable 1 key for proxy container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment1Value</td>
      <td>Environment variable 1 plain-text value for proxy container (if ProxyEnvironment1Key is set, set either ProxyEnvironment1Value or ProxyEnvironment1SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment1SecretModule</td>
      <td>Environment variable 1 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for proxy container (if ProxyEnvironment1Key is set, set either ProxyEnvironment1Value or ProxyEnvironment1SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment2Key</td>
      <td>Environment variable 2 key for proxy container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment2Value</td>
      <td>Environment variable 2 plain-text value for proxy container (if ProxyEnvironment2Key is set, set either ProxyEnvironment2Value or ProxyEnvironment2SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment2SecretModule</td>
      <td>Environment variable 2 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for proxy container (if ProxyEnvironment2Key is set, set either ProxyEnvironment2Value or ProxyEnvironment2SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment3Key</td>
      <td>Environment variable 3 key for proxy container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment3Value</td>
      <td>Environment variable 3 plain-text value for proxy container (if ProxyEnvironment3Key is set, set either ProxyEnvironment3Value or ProxyEnvironment3SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment3SecretModule</td>
      <td>Environment variable 3 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for proxy container (if ProxyEnvironment3Key is set, set either ProxyEnvironment3Value or ProxyEnvironment3SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment4Key</td>
      <td>Environment variable 4 key for proxy container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment4Value</td>
      <td>Environment variable 4 plain-text value for proxy container (if ProxyEnvironment4Key is set, set either ProxyEnvironment4Value or ProxyEnvironment4SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment4SecretModule</td>
      <td>Environment variable 4 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for proxy container (if ProxyEnvironment4Key is set, set either ProxyEnvironment4Value or ProxyEnvironment4SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment5Key</td>
      <td>Environment variable 5 key for proxy container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment5Value</td>
      <td>Environment variable 5 plain-text value for proxy container (if ProxyEnvironment5Key is set, set either ProxyEnvironment5Value or ProxyEnvironment5SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>ProxyEnvironment5SecretModule</td>
      <td>Environment variable 5 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for proxy container (if ProxyEnvironment5Key is set, set either ProxyEnvironment5Value or ProxyEnvironment5SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppImage</td>
      <td>The Docker image to use for the app container. You can use images in the Docker Hub registry or specify other repositories (repository-url/image:tag). If the repository is private, set AppImageSecretModule as well!</td>
      <td>widdix/hello:v1</td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppImageSecretModule</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> which contains the repository credentials for private registry authentication</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppPort</td>
      <td>The port exposed by the app container that receives traffic from the load balancer or the proxy container (AppPort != ProxyPort != SidecarPort; ignored if TargetModule is not set)</td>
      <td>80</td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment1Key</td>
      <td>Environment variable 1 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment1Value</td>
      <td>Environment variable 1 plain-text value for app container (if AppEnvironment1Key is set, set either AppEnvironment1Value or AppEnvironment1SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment1SecretModule</td>
      <td>Environment variable 1 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for app container (if AppEnvironment1Key is set, set either AppEnvironment1Value or AppEnvironment1SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment2Key</td>
      <td>Environment variable 2 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment2Value</td>
      <td>Environment variable 2 plain-text value for app container (if AppEnvironment2Key is set, set either AppEnvironment2Value or AppEnvironment2SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment2SecretModule</td>
      <td>Environment variable 2 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for app container (if AppEnvironment2Key is set, set either AppEnvironment2Value or AppEnvironment2SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment3Key</td>
      <td>Environment variable 3 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment3Value</td>
      <td>Environment variable 3 plain-text value for app container (if AppEnvironment3Key is set, set either AppEnvironment3Value or AppEnvironment3SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment3SecretModule</td>
      <td>Environment variable 3 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for app container (if AppEnvironment3Key is set, set either AppEnvironment3Value or AppEnvironment3SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment4Key</td>
      <td>Environment variable 4 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment4Value</td>
      <td>Environment variable 4 plain-text value for app container (if AppEnvironment4Key is set, set either AppEnvironment4Value or AppEnvironment4SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment4SecretModule</td>
      <td>Environment variable 4 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for app container (if AppEnvironment4Key is set, set either AppEnvironment4Value or AppEnvironment4SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment5Key</td>
      <td>Environment variable 5 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment5Value</td>
      <td>Environment variable 5 plain-text value for app container (if AppEnvironment5Key is set, set either AppEnvironment5Value or AppEnvironment5SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment5SecretModule</td>
      <td>Environment variable 5 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for app container (if AppEnvironment5Key is set, set either AppEnvironment5Value or AppEnvironment5SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment6Key</td>
      <td>Environment variable 6 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment6Value</td>
      <td>Environment variable 6 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment7Key</td>
      <td>Environment variable 7 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment7Value</td>
      <td>Environment variable 7 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment8Key</td>
      <td>Environment variable 8 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment8Value</td>
      <td>Environment variable 8 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment9Key</td>
      <td>Environment variable 9 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment9Value</td>
      <td>Environment variable 9 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment10Key</td>
      <td>Environment variable 10 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment10Value</td>
      <td>Environment variable 10 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment11Key</td>
      <td>Environment variable 11 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment11Value</td>
      <td>Environment variable 11 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment12Key</td>
      <td>Environment variable 12 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment12Value</td>
      <td>Environment variable 12 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment13Key</td>
      <td>Environment variable 13 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment13Value</td>
      <td>Environment variable 13 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment14Key</td>
      <td>Environment variable 14 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment14Value</td>
      <td>Environment variable 14 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment15Key</td>
      <td>Environment variable 15 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment15Value</td>
      <td>Environment variable 15 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment16Key</td>
      <td>Environment variable 16 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment16Value</td>
      <td>Environment variable 16 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment17Key</td>
      <td>Environment variable 17 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment17Value</td>
      <td>Environment variable 17 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment18Key</td>
      <td>Environment variable 18 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment18Value</td>
      <td>Environment variable 18 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment19Key</td>
      <td>Environment variable 19 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment19Value</td>
      <td>Environment variable 19 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment20Key</td>
      <td>Environment variable 20 key for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>AppEnvironment20Value</td>
      <td>Environment variable 20 plain-text value for app container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarImage</td>
      <td>Docker image to use for the sidecar container. You can use images in the Docker Hub registry or specify other repositories (repository-url/image:tag). If the repository is private, set SidecarImageSecretModule as well!</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarImageSecretModule</td>
      <td>Stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> which contains the repository credentials for private registry authentication</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarPort</td>
      <td>The port exposed by the sidecar container reachable from the app container on host localhost (SidecarPort != ProxyPort != AppPort)</td>
      <td>9000</td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarProtocol</td>
      <td>The protocol used by the sidecar container reachable from the app container on host localhost.</td>
      <td>tcp</td>
      <td>no</td>
      <td>[tcp, udp]</td>
    </tr>
    <tr>
      <td>SidecarEnvironment1Key</td>
      <td>Environment variable 1 key for sidecar container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment1Value</td>
      <td>Environment variable 1 plain-text value for sidecar container (if SidecarEnvironment1Key is set, set either SidecarEnvironment1Value or SidecarEnvironment1SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment1SecretModule</td>
      <td>Environment variable 1 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for sidecar container (if SidecarEnvironment1Key is set, set either SidecarEnvironment1Value or SidecarEnvironment1SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment2Key</td>
      <td>Environment variable 2 key for sidecar container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment2Value</td>
      <td>Environment variable 2 plain-text value for sidecar container (if SidecarEnvironment2Key is set, set either SidecarEnvironment2Value or SidecarEnvironment2SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment2SecretModule</td>
      <td>Environment variable 2 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for sidecar container (if SidecarEnvironment2Key is set, set either SidecarEnvironment2Value or SidecarEnvironment2SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment3Key</td>
      <td>Environment variable 3 key for sidecar container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment3Value</td>
      <td>Environment variable 3 plain-text value for sidecar container (if SidecarEnvironment3Key is set, set either SidecarEnvironment3Value or SidecarEnvironment3SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment3SecretModule</td>
      <td>Environment variable 3 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for sidecar container (if SidecarEnvironment3Key is set, set either SidecarEnvironment3Value or SidecarEnvironment3SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment4Key</td>
      <td>Environment variable 4 key for sidecar container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment4Value</td>
      <td>Environment variable 4 plain-text value for sidecar container (if SidecarEnvironment4Key is set, set either SidecarEnvironment4Value or SidecarEnvironment4SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment4SecretModule</td>
      <td>Environment variable 4 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for sidecar container (if SidecarEnvironment4Key is set, set either SidecarEnvironment4Value or SidecarEnvironment4SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment5Key</td>
      <td>Environment variable 5 key for sidecar container</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment5Value</td>
      <td>Environment variable 5 plain-text value for sidecar container (if SidecarEnvironment5Key is set, set either SidecarEnvironment5Value or SidecarEnvironment5SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>SidecarEnvironment5SecretModule</td>
      <td>Environment variable 5 stack name of <a href="https://www.npmjs.com/package/@cfn-modules/secret">secret module</a> for sidecar container (if SidecarEnvironment5Key is set, set either SidecarEnvironment5Value or SidecarEnvironment5SecretModule)</td>
      <td></td>
      <td>no</td>
      <td></td>
    </tr>
    <tr>
      <td>Cpu</td>
      <td>The minimum number of vCPUs to reserve for the container</td>
      <td>0.25</td>
      <td>no</td>
      <td>[0.25, 0.5, 1, 2, 4]</td>
    </tr>
    <tr>
      <td>Memory</td>
      <td>The amount (in GB) of memory used by the task</td>
      <td>0.5</td>
      <td>no</td>
      <td>[0.5, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30]</td>
    </tr>
    <tr>
      <td>DesiredCount</td>
      <td>The number of simultaneous tasks, that you want to run on the cluster</td>
      <td>2</td>
      <td>no</td>
      <td>1-N</td>
    </tr>
    <tr>
      <td>MaxCapacity</td>
      <td>The maximum number of simultaneous tasks, that you want to run on the cluster</td>
      <td>4</td>
      <td>no</td>
      <td>1-N</td>
    </tr>
    <tr>
      <td>MinCapacity</td>
      <td>The minimum number of simultaneous tasks, that you want to run on the cluster</td>
      <td>2</td>
      <td>no</td>
      <td>1-N</td>
    </tr>
    <tr>
      <td>LogsRetentionInDays</td>
      <td>Specifies the number of days you want to retain log events in the specified log group</td>
      <td>14</td>
      <td>no</td>
      <td>[1, 3, 5, 7, 14, 30, 60, 90, 120, 150, 180, 365, 400, 545, 731, 1827, 3653]</td>
    </tr>
    <tr>
      <td>SubnetsReach</td>
      <td>Should the service have direct access to the Internet or do you prefer private subnets with NAT?</td>
      <td>Public</td>
      <td>no</td>
      <td>[Public, Private]</td>
    </tr>
    <tr>
      <td>AutoScaling</td>
      <td>Scale number of tasks based on CPU load?</td>
      <td>true</td>
      <td>no</td>
      <td>[true, false]</td>
    </tr>
    <tr>
      <td>HealthCheckGracePeriodSeconds</td>
      <td>The period of time, in seconds, that the Amazon ECS service scheduler ignores unhealthy Elastic Load Balancing target health checks after a task has first started (ignored if TargetModule is not set)</td>
      <td>60</td>
      <td>no</td>
      <td>0-1800</td>
    </tr>
    <tr>
      <td>Spot</td>
      <td>Run workload on spot capacity?</td>
      <td>false</td>
      <td>no</td>
      <td>[true, false]</td>
    </tr>
    <tr>
      <td>CpuArchitecture</td>
      <td>The CPU architecture of the container.</td>
      <td>X86_64</td>
      <td>no</td>
      <td>[X86_64, ARM64]</td>
    </tr>
    <tr>
      <td>OperatingSystemFamily</td>
      <td>The operating system family of the container.</td>
      <td>LINUX</td>
      <td>no</td>
      <td>[LINUX, WINDOWS_SERVER_2004_CORE,  WINDOWS_SERVER_2016_FULL,  WINDOWS_SERVER_2019_CORE,  WINDOWS_SERVER_2019_FULL,  WINDOWS_SERVER_2022_CORE, WINDOWS_SERVER_2022_FULL,  WINDOWS_SERVER_20H2_CORE]</td>
    </tr>
    <tr>
      <td>ExecuteCommand</td>
      <td>Enable or disable ECS execute command</td>
      <td>false</td>
      <td>no</td>
      <td>[false, true]</td>
    </tr>
  </tbody>
</table>

## Outputs

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Interface</th>
      <th>Description</th>
      <th>Exported?</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ModuleId</td>
      <td>global</td>
      <td>Id of the module</td>
      <td>no</td>
    </tr>
    <tr>
      <td>ModuleVersion</td>
      <td>global</td>
      <td>Version of the module</td>
      <td>no</td>
    </tr>
    <tr>
      <td>StackName</td>
      <td>global</td>
      <td>Name of the stack (used to pass module references)</td>
      <td>no</td>
    </tr>
    <tr>
      <td>TaskRoleArn</td>
      <td></td>
      <td>IAM Role ARN of task</td>
      <td>yes</td>
    </tr>
  </tbody>
</table>

## Private repositories

To fetch Docker images from private repositories, you have to provide the repository credentials via AWS Secrets Manager. Go to AWS Secrets Manager and create a new secret of type *other type*) with the plaintext value:

```json
{
  "username": "DOCKERHUB_USERNAME",
  "password": "DOCKERHUB_PASSWORD"
}
```

Use the [secret module](https://github.com/cfn-modules/secret) wrapper to use the secret within cfn-modules.

```
---
AWSTemplateFormatVersion: '2010-09-09'
Description: 'cfn-modules example'
Resources:
  Secret:
    Type: 'AWS::CloudFormation::Stack'
    Properties:
      Parameters:
        Arn: 'arn:aws:secretsmanager:eu-west-1:111111111111:secret:name/of/secret' # TODO replace with your secret ARN
      TemplateURL: './node_modules/@cfn-modules/secret/wrapper.yml'
```

The following image prameters support a secret:

| Parameter        | Secret               |
| ------------ | ------------------------ |
| ProxyImage   | ProxyImageSecretModule   | 
| AppImage     | AppImageSecretModule     |
| SidecarImage | SidecarImageSecretModule |

## Migration Guides

### Migrate to v2

* Rename `AmbassadorImage` to `ProxyImage`.
* Rename `AmbassadorPort` to `ProxyPort`.
* Rename `AmbassadorEnvironment1Key` to `ProxyEnvironment1Key`.
* Rename `AmbassadorEnvironment1Value` to `ProxyEnvironment1Value`.
* Rename `AmbassadorEnvironment2Key` to `ProxyEnvironment2Key`.
* Rename `AmbassadorEnvironment2Value` to `ProxyEnvironment2Value`.
* Rename `AmbassadorEnvironment3Key` to `ProxyEnvironment3Key`.
* Rename `AmbassadorEnvironment3Value` to `ProxyEnvironment3Value`.
