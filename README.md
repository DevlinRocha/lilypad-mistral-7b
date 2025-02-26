# Lilypad Mistral 7B

Run [Mistral 7B](https://ollama.com/library/mistral) on Lilypad Network.

## Getting Started

```sh
export WEB3_PRIVATE_KEY=WEB3_PRIVATE_KEY

lilypad run github.com/DevlinRocha/lilypad-mistral-7b:v0.0.0 -i input=$(echo '{"prompt": "What is the animal order of the frog", "system": "You are a helpful AI assistant", "temperature": "0.8", "num_ctx": "1024", "num_predict": "1024"}' | base64 -w 0)
```

### Valid Parameters and Values
> \* === Required

| Parameter      | Description                                                                                           | Default Value  
| -------------- | ----------------------------------------------------------------------------------------------------- | ------------- |
| prompt*        | Message from the user.                                                                                | `""`          |
| system         | System prompt for the model.                                                                          | `""`          |
| num_ctx        | Sets the size of the context window used to generate the next token.                                  | `2048`        |
| temperature    | The temperature of the model. Increasing the temperature will make the model answer more creatively.  | `0.8`         |
| num_predict    | Maximum number of tokens to predict when generating text.                                             | `-1`          |