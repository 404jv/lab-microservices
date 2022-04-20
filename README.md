## Anotações
O decorator `@Module` do Nest é para unir diversas classes em um módulo. Exemplo:
```ts
@Module({
  imports: [],
  controllers: [AppController],
  providers: [AppService],
})
```
Os controllers como o próprio nome já diz são os controllers da aplicação. Já os providers são todas as classes responsáveis por determinadas funcionalidades (Use case, services e etc...). 
