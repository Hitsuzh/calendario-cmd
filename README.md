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
)
```
