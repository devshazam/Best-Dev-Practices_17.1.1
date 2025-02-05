## Принцыпы обработки полей
	- actions c zod на сервере
		- useActionState => useFormState устарела⚠️
    - Controlled
        - const [formData, setFormData] = useState({ name: '', email: '' });
        - <input value={formData.name} />
        - const handleChange = (e) => { setFormData({ ...formData, [e.target.name]: e.target.value }); }
        - Без тега <form>
        - у каждого input есть свой value и onChange, которые хранятся и передаются через useState
    - Uncontrolled
        - С тегом <form>
        - у каждого input есть атрибут name, но нет value и onChange
        - Информация обрабатывается и передается при помощи 
            `const formData = new FormData(event.target)`
    - Сторонние библиотеки
        - ⛔React-Hook-Form
            ⛔- Не универсальная = для каждой UI библиотеки требуется свой пакет
            - AntD - https://www.react-hook-form.com/resources/3rd-party-bindings/
            - https://www.freecodecamp.org/news/react-form-validation-zod-react-hook-form/

