# Redis [Pub/Sub (Publish/Subscribe)](https://redis.io/docs/latest/develop/interact/pubsub/)

Redis Pub/Sub is a messaging pattern where senders (publishers) send messages to channels, and receivers (subscribers) subscribe to channels to receive messages. It is commonly used for real-time messaging and communication between applications or services.

## Key Concepts
1. **Channel**: A named message queue. Publishers send messages to a channel, and subscribers listen to it.
2. **Publisher**: Sends messages to a specific channel.
3. **Subscriber**: Listens to a channel to receive messages.

## How It Works
1. A subscriber subscribes to one or more channels using the `SUBSCRIBE` command.
2. A publisher sends a message to a channel using the `PUBLISH` command.
3. Redis delivers the message to all the subscribers of the channel.

## Commands
- **`SUBSCRIBE channel_name`**: Subscribes to a channel.
- **`PUBLISH channel_name message`**: Publishes a message to a channel.
- **`UNSUBSCRIBE channel_name`**: Unsubscribes from a channel.
- **`PSUBSCRIBE pattern`**: Subscribes to channels matching a pattern (e.g., `news.*`).
- **`PUNSUBSCRIBE pattern`**: Unsubscribes from channels matching a pattern.

## Example

### 1. Start a Subscriber
```bash
redis-cli
> SUBSCRIBE mychannel