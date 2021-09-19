# Containerize-Todo-App-dts

Ini adalah homework docker containerizing todo apps.  
Dicontainerize oleh Rizqi Pratama.

Docker Image : docker pull rizqipratama1st/todoapp:1  
Link Docker Hub : <https://hub.docker.com/r/rizqipratama1st/todoapp>

Image ini tak akan berjalan tanpa environment yang sudah ditentukan buka file .env untuk mengaturnya yang terpenting adalah pada docker compose. dan bawah ini adalah envorenment yang dibutuhkan untuk menjalankan aplikasinya.

```yaml
      - DB_URI=URI_MONGO_DB
      - DB_NAME=NAMA_DATABASE_MONGO
      - DB_COLLECTION_NAME=NAMA_COLLECTION_DATABASE
```

namun jika belum ada punya database, kalian bisa pakai docker-compose.yaml yang ada. dan jangan lupa untuk menyesuaikan file .env yang ada, sesuaikan dengan preferensi kalian masing masing atau jangan ubah apapun. lalu jalankan dengan periintah ```docker-compose up```

## License

MIT License  
Copyright (c) 2019 Shubham Chadokar  
Copyright (c) 2021 Rizqi Pratama
