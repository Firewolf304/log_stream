README

About:
 * This project is a log_stream with configuration capabilities.
 * It allows for specifying the log type and configuring it accordingly.

Some info:
 * The basic principle of work is implemented on "streams", which allows you to work more efficiently with data. A little synchronization is used to "attempt" to merge messages, but because the script is damp, then its fuck

Using:
 * To use the log_stream, follow this syntax:
   ```cpp
   classname[type log] << "message"
   ```

Examples:
 
1. Disabling a log type and configuring the log_stream:
   ```cpp
   firewolf::streams::logger output;
   output.allowed_type[firewolf::streams::logger::DEBUG] = false;
   output.config->show_time = true;
   output.config->wait = std::chrono::milliseconds(200);
   ```

2. Simple logging a message using the log_stream:
   ```cpp
   output << "1331";
   ```

3. Logging a message with a specific log type:
   ```cpp
   output[firewolf::streams::logger::DEBUG] << "test";
   ```
