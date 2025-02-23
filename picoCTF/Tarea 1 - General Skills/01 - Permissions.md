## Descripción
Can you read files in the root file? The system admin has provisioned an account for you on the main serve

## Solución
Se ve que al usar sudo -l e ingresar la contraseña del usuario actual da la oportunidad de ver que programas tienen beneficios de sudo
Entre estos está vi y cuando se ejecuta sudo vi se abre la interfaz de vim
Para ejecutar comandos se usa `:! comando`
Por lo tanto se usa `:! cat challenge/metadata.json`
```
picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}
```
