
generator client {
  provider = "prisma-client-js"
}

datasource db {
  	provider 	= "postgresql"
  	url       	= env("DATABASE_URL")
	shadowDatabaseUrl = env("SHADOW_DATABASE_URL")
}

model User {
	id              	Int       	@id @default(autoincrement())
				      			@id @default(cuid()) // генерация уникального id
	// String, Int, enum
	arrayCode			Int[]
	name				String?
	email			String		@unique
	colors			String[] 		@default(["red", "blue", "green"])


	super			Boolean   	@default(false)
								@default("DefaultText") // текст по умолчанию
								@default(5) // число по умолчанию
	desc				Json      	@default("{ \"hello\": \"world\" }") // json
	phone			String?
	orders			Order[]
	createdAt       	DateTime  	@default(now())

	 @@unique([email, token]) // уникальное совместное значение - те вместе эти поля имеют уникальное значение

}

model Order {
	id            	Int       	@id @default(autoincrement())
		// Описание характеристик заказа - которые клиент вводит в input
	feature       	String
		// Дополнительное описание - свободное содержание
	description   	String?
		// Итоговая цена товара
	price         	Float
		// Категория товара
	category      	String?
		// Номер офиса
	office        	Int     	@default(0)
		// Скидка
	discount      	Int?
	payId         	String?
	orderStatus   	Boolean   	@default(false)
	doneStatus    	Boolean   	@default(false)
	payStatus     	Boolean   	@default(false)
	userId			Int
  	user	        User 		@relation(fields: [userId], references: [id])
	images			Image[]
		// Вместо ID  используем email
	responsibleId	String?
	doneAt			DateTime?
  	createdAt     	DateTime  	@default(now())
} 

model Image {
  id            Int         @id @default(autoincrement())
  orderId		Int
  order         Order 		@relation(fields: [orderId], references: [id])
  url			String
  createdAt     DateTime  	@default(now())
}

