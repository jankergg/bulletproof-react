# Error Handling

### API Errors

Set up an interceptor for handling errors. You might want to fire a notification toast to notify users that something went wrong.

### In App Errors

Use error boundaries to handle errors that happen in the react tree. It is very popular to set only 1 single error boundary for the entire application, which would blow the entire application when an error occurs. That's why you should have more error boundaries on more specific parts of the application. That way if an error occurs the app will still work without the need to restart it.

### Error Tracking

You should track any error that occur in production. Although it could be implemented by your own API, it is a better idea to use tools like [Sentry](https://sentry.io/). It will report any issue that breaks the app. You will also be able to see on which platform, browser etc. did it occur. Make sure to upload source maps to sentry to see on which line in your source code did the error happen.