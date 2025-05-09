## Изменена система атрибутов и покемонов (урон и атака покемона увеличиваются от старого показателя атрибута)
   Playerstst.java
изменены 
   public double getElementalSpiritPower()
   public double getElementalSpiritDefense()


## Награда за убийство игрока с активным покемоном
   Player.java
изменены
   public boolean doDie(Creature killer)

   Config.java
изменены и добавлены переменные
   // Spirit Rewards (новые настройки)

   PvpRewardItem.ini
Добавлен конфиг


## Изменена система покемона (заточка атрибута увеличивает силу покемона)
   PlayerStat
изменены
   getElementalSpiritPower()
   getElementalSpiritDefense()


## Изменение цвета ника в зависимости от активного покемона (не сохраняется при релоге)
   Player.java
добавлен
   private void setSpiritColor()
изменен
   changeElementalSpirit()


##Механика заточки атрибутом 
   Добавлены ElementalAttributeData.xml
изменен
   RequestExEnchantItemAttribute.java // Заточка для брони одним атрибутом
В дату добавлены камни атрибута 0-150 со скилам (из GOD)
В дату Ы грейда добавлен 		
   <set name="element_enabled" val="true" />


##Механика подсчета стоимости персонажа от экипировки, уровня заточки, уровня покемона и уровня персонажа
   Player.java
добавлен
   public void calculateAndSetEquippedItemsPrice() //Выставляет в титутл сумму стоимости надетой экипировки из итемдаты
изменен
   tryLoadSpirits() //Добавляет обновление подсчета стоимости и цвета (calculateAndSetEquippedItemsPrice();)	
   
   Сonfig.java
добавлен
   // Коэффициенты для расчета стоимости персонажа
   
   PvpRewardItem.ini
добавлен конфиг

   Inventory.java
Изменен
   ChangeRecoder{} //Добавляет обновление подсчета стоимости 

   PlayerStat.Java
изменен
   public boolean addLevel(byte value) // добавлен calculateAndSetEquippedItemsPrice();

   ElementalSpirit.java
изменены
   private void levelUp() //
   public void reduceLevel() //


