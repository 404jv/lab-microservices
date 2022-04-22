## Anotações
> 💡 O decorator `@Module` do Nest é para unir diversas classes em um módulo. Exemplo:
```ts
@Module({
  imports: [],
  controllers: [AppController],
  providers: [AppService],
})
```
Os controllers como o próprio nome já diz são os controllers da aplicação. Já os providers são todas as classes responsáveis por determinadas funcionalidades (Use case, services e etc...). 

> 💡 Podemos gerar diversos arquivos com o client Nest, por exemplo, services, controllers, class,decorator, gateway, middleware e etc...

Para saber todos os tipos de arquivos que o Nest gera:
```bash
$ nest generate -h
```

Exemplo de criação de um modules:
```bash
$ neste generate module http
```

> 💡 Para fazer um código aleatório para usar como secret:
```bash
$ openssl rand -hex 32
```
Isso vai gerar um código em hexadecimal de 32 caracteres.

> 💡 Para fazer um module poder ser usado por outros modules, é preciso colocar ele no `exports` do decorator `@Module`, por exemplo:

```ts
@Module({
  providers: [PrismaService],
  exports: [PrismaService],
})
export class DatabaseModule {}
```
Aqui o module database permite que o `PrismaService` seja importado por outras partes da aplicação.

