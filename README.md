# ![LOGO](logo.png) Cloud Pub/Sub **flow**ground Connector

## Description

A generated **flow**ground connector for the Cloud Pub/Sub API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/pubsub/v1/swagger.json<br/>
Generated at: 2019-05-23T12:13:34+03:00

## API Description

Provides reliable, many-to-many, asynchronous messaging between applications.


## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Updates an existing snapshot. Snapshots are used in<br/>
> <a href="https://cloud.google.com/pubsub/docs/replay-overview">Seek</a><br/>
> operations, which allow<br/>
> you to manage message acknowledgments in bulk. That is, you can set the<br/>
> acknowledgment state of messages in an existing subscription to the state<br/>
> captured by a snapshot.<br><br><br/>
> <b>BETA:</b> This feature is part of a beta release. This API might be<br/>
> changed in backward-incompatible ways and is not recommended for production<br/>
> use. It is not subject to any SLA or deprecation policy.<br/>
> Note that certain properties of a snapshot are not modifiable.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The name of the snapshot.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a snapshot from the requested subscription. Snapshots are used in<br/>
> <a href="https://cloud.google.com/pubsub/docs/replay-overview">Seek</a><br/>
> operations, which allow<br/>
> you to manage message acknowledgments in bulk. That is, you can set the<br/>
> acknowledgment state of messages in an existing subscription to the state<br/>
> captured by a snapshot.<br/>
> <br><br><br/>
> <b>BETA:</b> This feature is part of a beta release. This API might be<br/>
> changed in backward-incompatible ways and is not recommended for production<br/>
> use. It is not subject to any SLA or deprecation policy.<br><br><br/>
> If the snapshot already exists, returns `ALREADY_EXISTS`.<br/>
> If the requested subscription doesn't exist, returns `NOT_FOUND`.<br/>
> If the backlog in the subscription is too old -- and the resulting snapshot<br/>
> would expire in less than 1 hour -- then `FAILED_PRECONDITION` is returned.<br/>
> See also the `Snapshot.expire_time` field. If the name is not provided in<br/>
> the request, the server will assign a random<br/>
> name for this snapshot on the same project as the subscription, conforming<br/>
> to the<br/>
> [resource name format](https://cloud.google.com/pubsub/docs/admin#resource_names).<br/>
> The generated name is populated in the returned Snapshot object. Note that<br/>
> for REST API requests, you must specify a name in the request.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Optional user-provided name for this snapshot.
If the name is not provided in the request, the server will assign a random
name for this snapshot on the same project as the subscription.
Note that for REST API requests, you must specify a name.  See the
<a href="https://cloud.google.com/pubsub/docs/admin#resource_names">
resource name rules</a>.
Format is `projects/{project}/snapshots/{snap}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the existing snapshots. Snapshots are used in<br/>
> <a href="https://cloud.google.com/pubsub/docs/replay-overview">Seek</a><br/>
> operations, which allow<br/>
> you to manage message acknowledgments in bulk. That is, you can set the<br/>
> acknowledgment state of messages in an existing subscription to the state<br/>
> captured by a snapshot.<br><br><br/>
> <b>BETA:</b> This feature is part of a beta release. This API might be<br/>
> changed in backward-incompatible ways and is not recommended for production<br/>
> use. It is not subject to any SLA or deprecation policy.

*Tags:* `projects`

#### Input Parameters
* `pageSize` - _optional_ - Maximum number of snapshots to return.
* `pageToken` - _optional_ - The value returned by the last `ListSnapshotsResponse`; indicates that this
is a continuation of a prior `ListSnapshots` call, and that the system
should return the next page of data.
* `project` - _required_ - The name of the project in which to list snapshots.
Format is `projects/{project-id}`.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists matching subscriptions.

*Tags:* `projects`

#### Input Parameters
* `pageSize` - _optional_ - Maximum number of subscriptions to return.
* `pageToken` - _optional_ - The value returned by the last `ListSubscriptionsResponse`; indicates that
this is a continuation of a prior `ListSubscriptions` call, and that the
system should return the next page of data.
* `project` - _required_ - The name of the project in which to list subscriptions.
Format is `projects/{project-id}`.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists matching topics.

*Tags:* `projects`

#### Input Parameters
* `pageSize` - _optional_ - Maximum number of topics to return.
* `pageToken` - _optional_ - The value returned by the last `ListTopicsResponse`; indicates that this is
a continuation of a prior `ListTopics` call, and that the system should
return the next page of data.
* `project` - _required_ - The name of the project in which to list topics.
Format is `projects/{project-id}`.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the access control policy for a resource.<br/>
> Returns an empty policy if the resource exists and does not have a policy<br/>
> set.

*Tags:* `projects`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Sets the access control policy on the specified resource. Replaces any<br/>
> existing policy.

*Tags:* `projects`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being specified.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns permissions that a caller has on the specified resource.<br/>
> If the resource does not exist, this will return an empty set of<br/>
> permissions, not a NOT_FOUND error.<br/>
> <br/>
> Note: This operation is designed to be used for building permission-aware<br/>
> UIs and command-line tools, not for authorization checking. This operation<br/>
> may "fail open" without warning.

*Tags:* `projects`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy detail is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Removes an existing snapshot. Snapshots are used in<br/>
> <a href="https://cloud.google.com/pubsub/docs/replay-overview">Seek</a><br/>
> operations, which allow<br/>
> you to manage message acknowledgments in bulk. That is, you can set the<br/>
> acknowledgment state of messages in an existing subscription to the state<br/>
> captured by a snapshot.<br><br><br/>
> <b>BETA:</b> This feature is part of a beta release. This API might be<br/>
> changed in backward-incompatible ways and is not recommended for production<br/>
> use. It is not subject to any SLA or deprecation policy.<br/>
> When the snapshot is deleted, all messages retained in the snapshot<br/>
> are immediately dropped. After a snapshot is deleted, a new one may be<br/>
> created with the same name, but the new one has no association with the old<br/>
> snapshot or its subscription, unless the same subscription is specified.

*Tags:* `projects`

#### Input Parameters
* `snapshot` - _required_ - The name of the snapshot to delete.
Format is `projects/{project}/snapshots/{snap}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the configuration details of a snapshot. Snapshots are used in<br/>
> <a href="https://cloud.google.com/pubsub/docs/replay-overview">Seek</a><br/>
> operations, which allow you to manage message acknowledgments in bulk. That<br/>
> is, you can set the acknowledgment state of messages in an existing<br/>
> subscription to the state captured by a snapshot.<br><br><br/>
> <b>BETA:</b> This feature is part of a beta release. This API might be<br/>
> changed in backward-incompatible ways and is not recommended for production<br/>
> use. It is not subject to any SLA or deprecation policy.

*Tags:* `projects`

#### Input Parameters
* `snapshot` - _required_ - The name of the snapshot to get.
Format is `projects/{project}/snapshots/{snap}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes an existing subscription. All messages retained in the subscription<br/>
> are immediately dropped. Calls to `Pull` after deletion will return<br/>
> `NOT_FOUND`. After a subscription is deleted, a new one may be created with<br/>
> the same name, but the new one has no association with the old<br/>
> subscription or its topic unless the same topic is specified.

*Tags:* `projects`

#### Input Parameters
* `subscription` - _required_ - The subscription to delete.
Format is `projects/{project}/subscriptions/{sub}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the configuration details of a subscription.

*Tags:* `projects`

#### Input Parameters
* `subscription` - _required_ - The name of the subscription to get.
Format is `projects/{project}/subscriptions/{sub}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Acknowledges the messages associated with the `ack_ids` in the<br/>
> `AcknowledgeRequest`. The Pub/Sub system can remove the relevant messages<br/>
> from the subscription.<br/>
> <br/>
> Acknowledging a message whose ack deadline has expired may succeed,<br/>
> but such a message may be redelivered later. Acknowledging a message more<br/>
> than once will not result in an error.

*Tags:* `projects`

#### Input Parameters
* `subscription` - _required_ - The subscription whose message is being acknowledged.
Format is `projects/{project}/subscriptions/{sub}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Modifies the ack deadline for a specific message. This method is useful<br/>
> to indicate that more time is needed to process a message by the<br/>
> subscriber, or to make the message available for redelivery if the<br/>
> processing was interrupted. Note that this does not modify the<br/>
> subscription-level `ackDeadlineSeconds` used for subsequent messages.

*Tags:* `projects`

#### Input Parameters
* `subscription` - _required_ - The name of the subscription.
Format is `projects/{project}/subscriptions/{sub}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Modifies the `PushConfig` for a specified subscription.<br/>
> <br/>
> This may be used to change a push subscription to a pull one (signified by<br/>
> an empty `PushConfig`) or vice versa, or change the endpoint URL and other<br/>
> attributes of a push subscription. Messages will accumulate for delivery<br/>
> continuously through the call regardless of changes to the `PushConfig`.

*Tags:* `projects`

#### Input Parameters
* `subscription` - _required_ - The name of the subscription.
Format is `projects/{project}/subscriptions/{sub}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Pulls messages from the server. The server may return `UNAVAILABLE` if<br/>
> there are too many concurrent pull requests pending for the given<br/>
> subscription.

*Tags:* `projects`

#### Input Parameters
* `subscription` - _required_ - The subscription from which messages should be pulled.
Format is `projects/{project}/subscriptions/{sub}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Seeks an existing subscription to a point in time or to a given snapshot,<br/>
> whichever is provided in the request. Snapshots are used in<br/>
> <a href="https://cloud.google.com/pubsub/docs/replay-overview">Seek</a><br/>
> operations, which allow<br/>
> you to manage message acknowledgments in bulk. That is, you can set the<br/>
> acknowledgment state of messages in an existing subscription to the state<br/>
> captured by a snapshot. Note that both the subscription and the snapshot<br/>
> must be on the same topic.<br><br><br/>
> <b>BETA:</b> This feature is part of a beta release. This API might be<br/>
> changed in backward-incompatible ways and is not recommended for production<br/>
> use. It is not subject to any SLA or deprecation policy.

*Tags:* `projects`

#### Input Parameters
* `subscription` - _required_ - The subscription to affect.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes the topic with the given name. Returns `NOT_FOUND` if the topic<br/>
> does not exist. After a topic is deleted, a new topic may be created with<br/>
> the same name; this is an entirely new topic with none of the old<br/>
> configuration or subscriptions. Existing subscriptions to this topic are<br/>
> not deleted, but their `topic` field is set to `_deleted-topic_`.

*Tags:* `projects`

#### Input Parameters
* `topic` - _required_ - Name of the topic to delete.
Format is `projects/{project}/topics/{topic}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the configuration of a topic.

*Tags:* `projects`

#### Input Parameters
* `topic` - _required_ - The name of the topic to get.
Format is `projects/{project}/topics/{topic}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the names of the snapshots on this topic. Snapshots are used in<br/>
> <a href="https://cloud.google.com/pubsub/docs/replay-overview">Seek</a><br/>
> operations, which allow<br/>
> you to manage message acknowledgments in bulk. That is, you can set the<br/>
> acknowledgment state of messages in an existing subscription to the state<br/>
> captured by a snapshot.<br><br><br/>
> <b>BETA:</b> This feature is part of a beta release. This API might be<br/>
> changed in backward-incompatible ways and is not recommended for production<br/>
> use. It is not subject to any SLA or deprecation policy.

*Tags:* `projects`

#### Input Parameters
* `pageSize` - _optional_ - Maximum number of snapshot names to return.
* `pageToken` - _optional_ - The value returned by the last `ListTopicSnapshotsResponse`; indicates
that this is a continuation of a prior `ListTopicSnapshots` call, and
that the system should return the next page of data.
* `topic` - _required_ - The name of the topic that snapshots are attached to.
Format is `projects/{project}/topics/{topic}`.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the names of the subscriptions on this topic.

*Tags:* `projects`

#### Input Parameters
* `pageSize` - _optional_ - Maximum number of subscription names to return.
* `pageToken` - _optional_ - The value returned by the last `ListTopicSubscriptionsResponse`; indicates
that this is a continuation of a prior `ListTopicSubscriptions` call, and
that the system should return the next page of data.
* `topic` - _required_ - The name of the topic that subscriptions are attached to.
Format is `projects/{project}/topics/{topic}`.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Adds one or more messages to the topic. Returns `NOT_FOUND` if the topic<br/>
> does not exist.

*Tags:* `projects`

#### Input Parameters
* `topic` - _required_ - The messages in the request will be published on this topic.
Format is `projects/{project}/topics/{topic}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-pubsub-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
