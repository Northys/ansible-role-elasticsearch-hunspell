# Ansible Role: Elasticsearch Hunspell

Clones [repository with dictonaries](https://github.com/titoBouzout/Dictionaries.git) and copies selected languages into elasticsearch config directory.

## Role Variables

```
hunspell_dictionary_clone_path: /tmp/northys.hunspell
```
A path where repository will be cloned. Can be changed to something like `/home/elasticsearch` if you don't want to clone it each system reboot.

```
hunspell_dictionary_path: /etc/elasticsearch/hunspell
```

A path where Elasticsearchs expects hunspell dictionaries.

```
hunspell_dictionaries: # language_code is path for elastic, language_file is filename in the repository
  - { language_code: cs_CZ, language_file: Czech}
```

A list of languages to copy into Elasticsearch hunspell directory. You have to specify language file name (without extension!), because the repository does not use ISO language codes.
