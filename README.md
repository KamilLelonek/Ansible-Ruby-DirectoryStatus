# Ansible-Ruby-DirectoryStatus

This is an example of ruby library to be executed by Ansible.

## Setup

    vagrant up

## Run

    vagrant provision

## Usage

You can find the usage by looking either at `stat.yml` or at library code itself (`library/stat`).

## Description

You can call action for given path:

      - name:     call stat action
        action:   stat dir_path=/
        register: stat
        
The `stat` will be the following json:

    {
      exists:    true/false
      directory: true/false (if file or when not exists)
      empty:     true/false/none (in case of file)
    }