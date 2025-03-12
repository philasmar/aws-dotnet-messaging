## Release 2025-02-20

### AWS.Messaging (0.9.4)
* Fix issue with fifo when a message is failed to process the later messages are not retried
* Update User-Agent string
* Avoid logging error during shutdown
### AWS.Messaging.Lambda (0.10.1)
* Update AWS.Messaging dependency
* Update project dependencies
### AWS.Messaging.Telemetry.OpenTelemetry (0.9.2)
* Update project dependencies

## Release 2025-01-13

### AWS.Messaging (0.9.3)
* Removes references to SNS in the EventBridge publisher documentation
* Update logic to make DefaultMessageManager fail on InvalidMessageHandlerSignatureException

## Release 2024-08-15

### AWS.Messaging (0.9.2)
* Add support for AddAWSMessageBus being invoked multiple times against the same ServiceCollection. This allows different modules to register their own handlers rather than requiring a centralized registration.

## Release 2024-08-02

### AWS.Messaging.Lambda (0.10.0)
* Add default visibility timeout for failed partial batch response.

## Release 2024-04-22

### AWS.Messaging (0.9.1)
* Adding the response to the publish operation
* Update User-Agent string
### AWS.Messaging.Lambda (0.9.1)
* Update project dependencies
### AWS.Messaging.Telemetry.OpenTelemetry (0.9.1)
* Update project dependencies

## Release 2024-03-26

### AWS.Messaging (0.9.0)
* **AWS.Messaging** is now in _**Developer Preview**_
### AWS.Messaging.Lambda (0.9.0)
* **AWS.Messaging.Lambda** is now in _**Developer Preview**_
### AWS.Messaging.Telemetry.OpenTelemetry (0.9.0)
* **AWS.Messaging.Telemetry.OpenTelemetry** is now in _**Developer Preview**_

## Release 2024-03-20

### AWS.Messaging (0.3.0-beta)
* Added back-off logic to the SQS Poller that can perform Exponential, Interval or disable back-offs entirely. The SQS Poller will now back-off before attempting to reach SQS in case of an exception.
* Added support for SourceLink
### AWS.Messaging.Lambda (0.1.1-beta)
* Added support for SourceLink
### AWS.Messaging.Telemetry.OpenTelemetry (0.1.1-beta)
* Added support for SourceLink

## Release 2024-03-08
### AWS.Messaging (0.2.0-beta)
* BREAKING CHANGE: Message content is no longer included by default in logs or exceptions. Call `EnableDataMessageLogging` during setup to re-enable.
* BREAKING CHANGE: Replaced `IsSQSExceptionFatal` with `IsExceptionFatal` to allow classifying a broader range of exceptions. Expanded the default list of fatal exceptions.
* BREAKING CHANGE: Renamed `PublishAsync` to `SendAsync on the SQS-specific publisher, and create separate interface definitions to clarify "publishing" vs. "sending" depending on the destination service.
* Allow overriding the destination and AWS service client on the service-specific publishers. This allows you to set the destination and credentials on a per-message basis, which may be useful for multi-tenant applications.
* Improved validation on ECS task metadata when deriving the default value for the message source on ECS.
* Improved documentation and examples around `IMessagePublisher`

## Release 2023-12-08
### AWS.Messaging (0.1.0-beta)
* Initial _**beta**_ release.
### AWS.Messaging.Lambda (0.1.0-beta)
* Initial _**beta**_ release.
### AWS.Messaging.Telemetry.OpenTelemetry (0.1.0-beta)
* Initial _**beta**_ release.