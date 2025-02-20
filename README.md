# Calendario
## Explicação:
Esse script foi desenvolvido para ser um calendario e identificar quais serão os anos bissextos

```markdown
set /a ano=%1
set /a bissexto=%ano% %% 4
set /a seculo=%ano% %% 100
set /a quadricentenario=%ano% %% 400
if %mes%==2 (
    if %bissexto%==0 (
        if not %seculo%==0 (
            set dias=29
        ) else if %quadricentenario%==0 (
            set dias=29
        )
    )
Essa parte do script é para descobrir o ano bissexto
```

```markdown
if %mes%==3 set dias=31
if %mes%==4 set dias=30
if %mes%==5 set dias=31
if %mes%==6 set dias=30
if %mes%==7 set dias=31
if %mes%==8 set dias=31
if %mes%==9 set dias=30
if %mes%==10 set dias=31
if %mes%==11 set dias=30
if %mes%==12 set dias=31

Essa parte foi usada para definir os dias de cada mês
```

```markdown
FOR : Repetiçao de execuçao do código 
IF : Executa o código com uma condição
SET : Para criar uma variálvel
ELSE : Aplicar condição

Alguns comandos utilizados
```

## Desafios e Soluções
Um dos peincipais desafios foi descobrir como iriamos fazer o script para descobrir os anos bissexto, mas com muita pesquisa conseguimos resolver usando o seguinte esquema : 
- 1  Se o ano for uniformemente divisível por 4, vá para a etapa 2. Caso contrário, vá para a etapa 5.
- 2  Se o ano for uniformemente divisível por 100, vá para a etapa 3. Caso contrário, vá para a etapa 4.
- 3  Se o ano for uniformemente divisível por 400, vá para a etapa 4. Caso contrário, vá para a etapa 5.
- 4  O ano é bissexto (tem 366 dias).
- 5  O ano não é um ano bissexto (tem 365 dias).
