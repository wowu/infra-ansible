# Infra - Ansible

Wprowadzenie do Ansible.

## Przykłady

### `1_simple_playbook`

Prosty playbook instalujący nginxa.

### `2_playbook_with_variables`

Kilka miejsc w których możemy definiować zmienne.

### `3_playbook_with_roles`

Rola tworząca użytkownika i rola instalująca serwer SSH.

## Zadanie praktyczne

Folder `4_lab`.

### Konfiguracja

1. Sprawdź czy możesz połączyć się z serwerem:

   ```bash
   ssh infra@infra.musur.pl -p 10##

   ## <- to numer serwera
   ```

2. Dodaj swój klucz ssh:

   ```bash
   ssh-copy-id -p 10## infra@infra.musur.pl

   # lub

   ssh infra@infra.musur.pl -p 10##
   touch ~/.ssh/authorized_keys
   nano ~/.ssh/authorized_keys
   ```

### Zadanie

- Skonfiguruj serwer wystawiający nginxa na porcie 80.
- Dodaj użytkownika `guest`.
- Uruchom w dockerze kontener [`containous/whoami`](https://hub.docker.com/r/containous/whoami) bindujący do interfejsu `127.0.0.1:3000`.
- Dodaj konfigurację nginxa sprawiającą że kontener jest dostepny pod adresem `infra.musur.pl:1003`.
