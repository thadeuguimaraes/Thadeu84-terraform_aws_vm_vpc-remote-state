# Terraform_aws_vm_vpcremote-state

Este projeto utiliza o Terraform para criar uma máquina virtual (VM) na AWS e fazer o deploy de uma aplicação nesta VM. Além disso, ele utiliza o recurso de remote state do Terraform para sincronizar o estado das suas infraestruturas na AWS

## Requisitos

Para utilizar este projeto, você precisa ter as seguintes ferramentas instaladas em sua máquina:

- Terraform (versão 1.0.0 ou superior)
- AWS CLI
  Além disso, é necessário possuir uma conta na AWS e configurar suas credenciais de acesso na AWS CLI.

## Estado Remoto

O estado desse projeto é armazenado em um bucket do S3 chamado matrix-revolution-remote-state, com a chave aws-vm/terraform.tfstatena us-east-1região.

## Provedor da AWS

Este projeto usa o provedor AWS, com a região definida como us-east-1. As tags padrão owner e managed-by são definidas como <NOME> e terraform, respectivamente.

## Dependências

Este projeto depende do estado do aws-vpcprojeto, que é armazenado no mesmo bucket S3 com a chave aws-vpc/terraform.tfstate. Os dados são recuperados usando a terraform_remote_state fonte de dados.
Alguns links úteis para o seu projeto:

## Links úteis

- Documentação do Terraform: https://www.terraform.io/docs/
- Documentação da AWS: https://aws.amazon.com/documentation/
- Guia de início rápido do Terraform: https://learn.hashicorp.com/terraform/getting-started/install.html
- Referência da linguagem do Terraform: https://www.terraform.io/docs/configuration/index.html
