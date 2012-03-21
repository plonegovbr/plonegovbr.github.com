Introdução
============

`github/plonegovbr`_ é o repositório de código produzido pelos membros da 
comunidade  `PloneGovBr <http://plone.org.br/gov>`_.

Este repositório segue as mesmas regras e práticas do 
`Collective <https://github.com/collective>`_ que é o coletivo de códigos 
criados pela comunidade Plone.

"Regras" do github/plonegovbr
===============================

Usando a termilogia do Github, o **plonegovbr** é uma organização e como tal
permite a criação de repositórios e times de usuários. Para facilitar a gestão
da organização definimos algumas regras:

- Todos os membros desta organização terão a permissão de ``Pull e Push`` para
  todos os repositórios aqui hospedados.
- Cada um dos repositórios terá donos (owners) que terão acesso 
  administrativo a eles.
- Abusos devem ser reportados através de um ticket no repositório 
  `plonegovbr.github.com`_.

Como conseguir acesso
========================

O primeiro passo é ter uma conta no `Github <https://github.com/>`_,
se você ainda não tem,
`crie uma gratuitamente <https://github.com/signup/free>`_.

Com sua conta criada, escolha uma das duas opções abaixo:

* Crie um ticket pedindo permissão através deste endereço:
  https://github.com/plonegovbr/plonegovbr.github.com/issues

* Ou faça o fork do repositório `plonegovbr.github.com`_, edite o arquivo
  ``permissions.cfg``, faça o commit, push e envie um Pull Request para nós
  (veja a seção abaixo para entender os detalhes).

Como gerenciar permissões e repositórios
==========================================

Visão geral
------------

Permissões são armazenadas no arquivo `permissions.cfg`_ no repositório
`plonegovbr.github.com`_.

Realize o fork do repositório 
`plonegovbr.github.com <https://github.com/plonegovbr/plonegovbr.github.com>`_
e edite o arquivo `permissions.cfg`_, realize o commit, push e inicie um
pull request através da interface do Github. 

Temos um script que é executado a cada 10min para verificar diferenças no
arquivo de permissões e atualizar o 
`plonegovbr <https://github.com/plonegovbr/>`_.

No arquivo `permissions.cfg`_ você encontrará uma lista de times e 
repositórios.

Times são representados por seções iniciadas com ``team:`` e repositórios
são seções iniciadas com ``repo:``.

Editando o arquivo permissions.cfg
---------------------------------------

Repositório criado, mas você não é o dono (owner)
    O repositório foi migrado de outra ferramenta e você não está com a
    permissão corretamente aplicada aqui? Adicione seu nome de usuário ao
    item ``owners =`` da seção de seu repositório.

Realizar o fork de um repositório existente de outro usuário ou organização
    Adicione uma nova seção::

        [repo:NOME_DO_REPOSITORIO]
        fork = DE_USUARIO_OU_ORGANIZACAO/NOME_DO_REPOSITORIO
        teams = colaboradores
        owners = MEU_NOME_DE_USUARIO

Criar um novo repositório
    Adicione uma nova seção::

        [repo:NOME_DO_NOVO_REPOSITORIO]
        teams = colaboradores
        owners = MY_NOME_DE_USUARIO

Adicionar você ao time de ``colaboradores`` (ou qualquer outro time)
   Vá até a seção ``[team:colaboradores]`` e adicione o seu nome ao final 
   da lista.

**POR FAVOR não utilize o botão de criar novo repositório da interface do 
Github, caso contrário a equipe que mantém esta organização terá que 
editar o aquivo permissions.cfg manualmente**

.. _`plonegovbr.github.com`: https://github.com/plonegovbr/plonegovbr.github.com
.. _`permissions.cfg`: https://github.com/plonegovbr/plonegovbr.github.com/blob/master/permissions.cfg
.. _`github/plonegovbr`: http://github.com/plonegovbr

