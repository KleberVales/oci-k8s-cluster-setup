# 🚀 Criação de um Cluster Kubernetes no OCI

Este repositório contém o passo a passo para criar e acessar um cluster Kubernetes no Oracle Cloud Infrastructure (OCI) utilizando o Cloud Shell.

## 📋 Pré-requisitos

- Conta ativa no Oracle Cloud
- Usuário com permissões de ClusterAdmin e VCN Admin
- Acesso ao Cloud Shell no console do OCI

## 🔧 Passo 1 - Acessar o Cloud Shell

No console da OCI, clique no ícone de Cloud Shell (canto superior direito).
Isso abrirá um terminal já autenticado com sua conta.

## ☸️ Passo 2 - Criar um Cluster Kubernetes

No Cloud Shell, execute:

```cloud shell

# Cria o cluster Kubernetes
oci ce cluster create \
--name meu-cluster \
--kubernetes-version v1.29.1 \
--compartment-id <OCID_DO_COMPARTMENT> \
--vcn-id <OCID_DA_VCN> \
--service-lb-subnet-ids '["<OCID_SUBNET>"]'

```
