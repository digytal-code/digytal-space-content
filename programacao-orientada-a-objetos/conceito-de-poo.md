# Conceito de POO

Você já ouviu falar a expressão linguagem de baixo e de alto nível ?

À medida que a tecnologia vem evoluindo, as linguagens de programação também e está transição natural que determina quando estamos nos referindo a linguagem de baixo e alto nível.

**Baixo nível**: São linguagens que estão mais próxima da interpretação da máquina diante do algoritmo desenvolvido. Exemplo: **Linguagem Assembly e C**

**Alto nível**: São linguagens que disponibilizam uma proposta de sintaxe (forma de escrever processos para serem executados pelo computador) mais próxima de interpretação humana. Exemplo: **Java, JavaScript, Python e C++**

Exemplo de um simples `Hello World` em **Assembly** versus **Python**:

{% tabs %}
{% tab title="Assembly" %}
```wasm
section	.text

   global _start   

_start: 

   mov	edx, len  

   mov	ecx, msg  

   mov	ebx, 1 

   mov	eax, 4  

   int	0x80   

   mov	eax, 1 

   int	0x80   

section	.data

msg	db	'Hello, world!',0xa

len	equ	$ - msg
```
{% endtab %}

{% tab title="Python" %}
```python
print('Hello, world!')
```
{% endtab %}
{% endtabs %}



