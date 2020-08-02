# email-worker-compose

docker-compose up -d
docker-compose exec db psql -U postgres -c '\l'
docker-compose exec db psql -U postgres -f /scripts/check.sql
docker-compose exec db psql -U postgres -d email_sender -c 'select * from emails'