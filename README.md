# Ansible-Ruby-DirectoryStatus

This is an example of ruby library to be executed by Ansible.

## Setup

    vagrant up

## Run

    vagrant provision

## Usage

You can find the usage by looking either at `status.yml` or at library code itself (`library/status`).

## Description

You can call action for given path:

      - name:     call status action
        status:   dir_path=/
        register: status_of_path
        
The `status_of_path` will be the following json:

    {
      exists:    true/false
      directory: true/false (if file or when not exists)
      empty:     true/false/none (in case of file)
    }
