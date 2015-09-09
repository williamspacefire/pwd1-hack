# PWD1 - Classe de Salt Escrita em HACK
PWD1 é uma classe criada para deixar a senha mais segura, usando uma chave definida por você para gerar as hashs, assim a hash da senha gerada será diferente para cada chave definida.
# Configuração
Primeiro abra a classe e atribua uma chave digitando caracteres aleatórios, não tem limite de caracteres
para a constante KEY.
```hack
const string KEY = "digite caracteres aleatórios aqui";
```

# Exemplo de Uso

### 1) Exemplo 1

Exemplo mostrando como o pwd1 pode ser usado
```hack
<?hh
include("pwd1.class.php");
$senha = pwd1::encrypt(md5("Aqui fica a senha"));
```

### 2) Exemplo 2

Uso recomendado da classe. 
<br>ATENÇÂO: com esse uso, a classe irá retornar um Exception caso nenhuma senha seja passada para a função encrypt()
```hack
<?hh
include("pwd1.class.php");
$pass = "minha senha é essa";
$senha = pwd1::encrypt(!empty($pass) ? md5($pass) : null);
echo $senha;
```
