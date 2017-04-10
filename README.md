# DeviceJS

Júlio Cesar Trindade: 20161011110018 / GitHub Nickname: JulioTrindade;<br/>
Wesley Giovane: 20141011110166 / GitHub Nickname:WesleyGiovane;<br/>
Júlio Cesar Fernandes: 20141011110344 / GitHub Nickname: jcesar732;<br/>
Linguagem: DeviceJS

## Resumo

**Observações MINORA**
Veja link na página da disciplina e use a sintaxe Markdown!!!

**Propósito da linguagem**: 

O DeviceJS tem como objetivo permitir que desenvolvedores familiarizados com bibliotecas de desenvolvimento da Web apliquem algo que aconteça dinamicamente no mundo físico.

**Paradgima da linguagem**: 

Procedural, visto que segue o conceito de um estado e de ações que manipulam esse estado, nele encontramos procedimentos que servem de mecanismos de estruturação. Podemos denominá-lo procedural por incluir procedimentos para estruturação.

**Data de criação**:
dd de mês de 2015

**Principal mantenedor**: 
- KeystoneJS

## Instalação e uso

**Como instalar?**
- O DeviceJS é um sistema distribuído;
- O DeviceJS pode distribuir um script em qualquer retransmissão capaz de executar o DeviceJS run-time. 

**Como usar?**
- Pode ser usado: em um banco de dados JSON distribuído em tempo real, que atualiza diretamente para o tempo de execução do DeviceJS. Em API baseada em objetos, baseada basicamente em base2 e Prototype. Em ganchos de serviço para drivers de dispositivo nativos para protocolos como: 6loWPAN, Z-Wave e ZigBee. Em um Catálogo que permite que dispositivos de todos os tipos sejam categorizados e cruzados em uma variedade de maneiras, e em APIs para lidar com JavaScript complexo, assíncrono, semelhante no conceito de  async.js.
- Execução: Os scripts e aplicativos escritos para DeviceJS podem executar e consequentemente controlar dispositivos em muitos locais. 
   
**Comandos:**
   
**Seletores:**
- Transformar toda a iluminação em um local vermelho:
```js
  dev$.byLocation("kitchen").setColor("red");
```
- Mudar todos os dispositivos marcados como uma "luz" para desligado:
```js
  dev$.byTag('light').setOff();
```
**Eventos:**
- Pop-up de alerta de caixa de diálogo em um 'clique':
```js
  dev$.byDeviceAlias('hallway-sensor').trigger('motion',function(){dev$.byLocation('hallway').setOn();});
```
**Sensor de movimento acionado de acordo com a movimentação no ambiente:**
```js
  function func1(){dev$.byTag('light').setOn();}dev$.trigger('motion', func1);
```
