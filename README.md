# mcpandlitellm

LiteLLM local como proxy OpenAI-compatible + Codex apuntando a ese proxy. OCI Generative AI ya expone APIs compatibles con OpenAI, y LiteLLM soporta OCI con credenciales manuales o con OCI SDK Signe

litelm.yaml
```
model_list:
  - model_name: oci-command
    litellm_params:
      model: oci/cohere.command-r-plus
      oci_config: "C:\\Users\\antonio\\.oci\\config"
      oci_profile: "DEFAULT"

general_settings:
  master_key: "sk-local-dev"
```


```
pip install 'litellm[proxy]'
litellm --config litellm.yaml --port 4000
```

