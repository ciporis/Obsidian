### OnCollisionEnter and OnCollisionExit
Работают только с Colliders и Rigidbody. В методах выполняются блоки кода при входе или выходе чужого коллайдера в(из) коллайдер(а) объекта, на котором висит компонент

### Physycs.OverlapSphere(Vector3 position, float radius)
Возвращает массив объектов, которые попадают в виртуальную сферу с  радиусом radius

### Rigidbody.AddExplosionForce(float explosionForce, Vector3 explosionPosition, float explosionRadius)
Применяет силу взрыва к указанной позиции на указанный радиус с указанной силой

### Object.Instantiate(Object original, Vector3 position, Quaternion rotation)
Создает объект в указанной позиции

### Gameobject.Destroy(Gameobject gameobject)
Уничтожает объект

### OnMouseUpAsButton()
В методе выполняется код при нажатии лкм на объект

### OnValidate()
Вызывается при изменениях в инспекторе

### GetComponent<>()
Возвращает компонент объекта
!!! ДОСТАТОЧНО ЭНЕРГОЕМКИЙ СПОСОБ !!!

### FindObjectOfType<>()
Находит первый активный загруженный объект указанного типа.

### FindObjectsOfType<>()
Gets a list of all loaded objects of type 

### Invoke(string method, delay)
Starts method with delay

### InvokeRepeating(string method, delay, repeatRate)
Starts method at delay from the start of game and repeat in every repeatRate