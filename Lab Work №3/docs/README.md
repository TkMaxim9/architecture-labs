# Лабораторная работа №3

Тема: Использование принципов проектирования на уровне методов и классов

Цель работы: Получить опыт проектирования и реализации модулей с использованием принципов KISS, YAGNI, DRY, SOLID и др.

## Диаграмма контейнеров

![image](https://camo.githubusercontent.com/30ffaf015eb490a394c769b1f3977cbfc54ca7594838a14b5e1fe4de77b61516/68747470733a2f2f696d672e706c616e74756d6c2e62697a2f706c616e74756d6c2f706e672f5a4c5054526e6a3535377474686e5a797165733852524e6d6e354533347135354e49736e4b482d6a794e66676873416c4c786a68383439384a4c65656744304b51344b386e514b576e3043794543516b6c7642754279702d38797754734d76733751534739536677546b757a767675767a75776c2d6d377457637778624e643354676e4d6a6f764f436d58535f7672326d55455676316a737145704d6b68786d6838754a323256384d7672736d4d726e5873396f5662316c73524c3279557353494b6956624d754d736a6d4658385562515834487437513462745366566f516d57765057794968526a3764337573734d4f794e6a34596c6c386778445a34745234725230496a6e6b734b77336c53612d7537547345426c4c32556d786a694b336b2d467551766343414a6f5f756e586a786c3236794450504c5a774a387463416c773579414b565874496f6a5f4968787962595558566c75466d68744d525a3776347045764f4a73676a4b4a454d3771457952704b4652333174656a326d5a446746666b662d6c4b6b5254684d35554861675a4135743849785935795841747a783168784243466d347254632d327837725a42756573304a3144633677784f597a6148694d7430684b306f5f4876425a373057483754304578734458366b7862324d4b5574576b5f59675a5635684c6f6e7a654830474646554e5a3057467146325a774a30724e755156576d5f3841357a7a4a37385050464b32557a63435866376b4b476d6f4d5174424d6874374c314f794579304d71386479417255316a6243747a686775427a6462314b6c714567434b6153786b4d472d6d706d34775a50707845684f466942553278305f71325557464b5a316b3970484c6d6b62356856613550765457725264754662694a6735365078716b4933544349684f6e7a773349776657536733446942675370506648687363554a75596c7356363358595641377a764b78467a30524e724148394936775836496f4c375134353170464d36364633446b55744f574d41624a357773724975346a525a4b356551495357544a586a7a3158306357773957725f653072476a747435772d5a593566306f75393377517236443750393272516a595074486b4d615949796b6a4e6767635a54386356356b2d3236346c51482d777776305943326c547444647056525a59596c697573314d794c637a6e665937675176584d6f6878524a5839666b37354c73656a71435a4f3371632d7039642d4e5679615a7375394238777765584a6f355555355f4c584c4450416a6f584b4c33354946684f6a5942487076354d7977515962506142784272454c69536163716c46363441634d52354777576e38312d74573276733634704178565a457432657167385f78677053684d586232566e2d4462777a4630343672436b77676c35655a53537a317565313631444a726c4a4c483878436b625965616159476d6b7473725a45624345644d30452d7638444e6f67774b7a4d45754943764c694e7453447674757a34754b73384a4a706561504f5531365950754d325a57566c59624b5835334352436a4d6b544a4c6d7977554f5957314e524671554c5a74544134797477624f664f484832356750746857413545477263556d6d7943756542327a4c51754735384e35345267725f72477267484f666f3179664e43794d3267754b7053384443754142752d42455f352d58634969696279696e6b423864567632375345505a58616c614355706f476c776262657a65315f5035386e45364e4a74676230634934703744515f643855776a7962716e6471364d364a763041513359706a4f474a4b67634e6c42306f537168774c5f7373523034515a6361424a32784a7737545350345f62346f6d7a6d756b646b307145764b2d484b685754723737466136304f4e794a644775545731576e762d673230366f35544a4a7063346855365061444a416662636b646f4b725f4266414f49556359492d3259475041436d3877693979494c5a64466e33564d61414366666777537650633657346b3855626b5569725738525a75556d30584e58544537542d6a5f574b30)

## Диаграмма компонентов

![](https://img.plantuml.biz/plantuml/png/ZLTRJnj757v7uZzCtPUrokKbZrKLObp5QcWTsseUhS4UwCfxw-uuYLL5CX0A5MeG4L8ZL2NjKr-1uc1iBdzXvY_qb_IScRtCsYQj4Ulr-bo-yvtR-674QSYxhZC_zvdjjPnkcv4lIm-MIm-Q9TyDV8zv_AlvkVavRdE74N4iXk9K_2txSBs6lrCYHk8MRkxWUYC6uaPkmzqv-QT_J5Qg5IB-50EGFiShiLRgrQLlomrIyaEsGBxpRDyZNv3IqteHVPHyZrFROw4L1NI15EhL5I9En1XyAiC5U2RUmltPeZX32797NABXGj5GNbstskieUGGOBn7X1TpSW843kOicgdx4DqDMV_faKgz5MpymL3sHlyfziangZBR9cjzc3YhMMDkESZfMXsvq4Eet-8uoAm7Q8Ffp75NCe-NvtDveHYn45malGxb580uW270YasCC5aA-KkOCmbJu7q3c0jW6DRa7KYFjQec8zy3ydKhCkHZBGp2_JPwnzRhVwZ2-ECk5F2H0iKPPxqMSkStoIsv5BWzYLt9FfrCUY2iYjx9K8fRwMgEAoePgG7ikHDhSf9oze3rjPGo9sfP7uYEc0Eti0xutubBPuA4TC62wIdjLwi3D8-fri78A-P9eFlAxNfk6FOi6DXBpoTeg5eha9zGdyCeIq09heUyuB8mI4oTOjm2l3-zZ94RsvS4aysJj-v9c7-I6AZjG-l8DCFouqQWkOfafxcyXAmT430ba2A4XuLeEsDubq1ThK4EKrtHqUNIk-ih7wbYBRmlfVKtv_nsizUK-_Ez0OeReL_wi4Xct8HRwXG9WGC8CPWuD8eEcGtj9EOv1x8eedQ7wy36j4cib21oxHJdqQqmjYLyckQvBlJOoAzxh_XHdu7vRrobYCZ1YED3tv5beSqOifBfOq41k0RjkMUXxu0munVmCvDw23WivnNkL2OmVhfY_yqpfJbSTH81HN67qquX_xBBGPfy2F4bY35gD1GCpDkKOKh8Nj-w0gEcqfVjKevA7W5WR7-YcmWWmDdYAb0zdWxGzpi8Dsj8utwa1YqNw6kF2SbEWFYULL0uVL6eiy2CRIWYQi59sgUtKMVZSRi5ugwY9KGtzThU5oQzKTTV60WcCLrC5q_R1ZfVLpB5Avq3FLZqWT15PgqhotbA93RauMASD0NjRGEOlyF5MyJECGomvD8fqV2N71aCBf46ZpW8q5UEsjxc44-4sflGmAOMXBfHpR1srlR3T3sQJ7GEBD1FHR6pPu4x9ZwbJq63lO6F2CfHRY-b4nfOwrPCXhbMqCigoFastxMs4T4Q7GZJojIumR0oOx2Duty71HQmAAaKyxBPuDvs3qu66K1vDsmqK_Nz0U7UgxOPPDS8eNbt7ySjUSWohxC4He4U-3gdBNlXX9rj9oFck2lCchN_GLxiZ_Mpku9dKCwpH198gs8HLTA96CIuSeZEl79iRRuJiwdORYElPBjIoJboe9Y195wG-z6F3oGVWzqoTGKRfi5NJu0nYmHbyTT_wdeaXsP09zpFMer5WAQp7d0S6g7WCw8DO2YeTUwcrwtJP8ZQZr5IrrPYZJrhvlLWhrnlgx6RXSgiNKGr5SrB6ib8xD1xhK8BBHFnchiD4FTCmDeKQ_zCIsMJ6KQjtbuQGQ4wEa7Hjo2FOjij4zQ3gMtqKoeAOi63s-bl0ZPc-m8K2MPsfbsiTe_RpVj88Sk9_gGuxJGIrg26X3gxP-PHOS4dvD-IIWsfw8fq4cUkc_sWKr3Jbu_DVShoRD9thel_H7eaBKoztR2RbvrZNgQluoudJSceH7TpRSAXlAEhV4UafU5OuamtvpZnKw1g0lPrsraxY9QytVV1LlQCTFg6zvkh4zZI6EyWyP5vR_GZx5m00)

  

## Диаграмма последовательностей

![](https://img.plantuml.biz/plantuml/png/TLJBQjj05DqBz0-3LyaYRUYoYv9WN5A26nCPkl5c8azY4KioqZXhnocKaa2X60fPjCqVo6vDbOULNxZp2_sItZiZsPQIOcn6cdFEt7lF6U_4aaTowFTjItgoBnXC88K4VgaH_ZxW9s7m29awXtkOms_8O0Q96kFwNbt1WdRqqotxEvemk4707uGbk9N2dC6Czb5ihZv1YeyCxd2Jj1O4entRiYtkoZ1YJHxm4n4n7ZFVB6rhWFLvhZVWWMGrfxNBu1hfAGceSOsWyO1NOBkjTmJB288dP4Z04zMe4spiEgqNxnjjLWyZiQdfRXZ8AEptdnpM55sFOrd8Cij3G_3pznKuV8UfdjeKXpAcTk6EkireYDIjkaIbUYIu54qXf1USr4CV--pkuHUFD-ezyr0LdsWTcjf2NU9WSQmNwlFIW5GNgKMDJ3VqkHTKLNwYmgEsA4LIXkMcS8lKnjkrWKHY45Q8-_pubBDM57Q7heWqwfHU5M-UWwzGrIfko0lCKQhEcRh0XGdMGnuBKz9Jeu9GUiUEYCuyLr1cyeYmhJSK0VQQmJSSzAEsUw6-u25ZfZxgBX_KHIMAjaKSfAxiHuNMWTDcBtqpoDYsrZOHMXYFG4S4tMUztDIL5K0avNuYnzZyVrQ1H99nZrfQNYWi_Ohbh4u0FtIkPtgITtH9KvpSJ5yekhyBiXTcjfKhRPKgoMKmHAlhMgc0Ga1zyZEn39PjwRTbhOFz2hCK39hfyAZlnRr2nRJVRPo9GA9Y6LtGYywdwfB2ZNaliqj7bfqv5F6mBzc6CtHT4SURwsvKxJROiitBDEsrsotsQdixxz3KXRlhCLpDShqjsofXbeeVn94JkgT2uapYNYUemTUrI2ObEo2fqQaxc3Fzx_mF)

## Модель БД

![](https://img.plantuml.biz/plantuml/png/ZLHTQjj047uNw0w3Nmej2UbhdcBiK09r2RLxW8qqr9jeLq6xUcXBmOaVIg6q57A1ti2uSMEQnBt2x1LwaiwkPHhBFwq4OdU-RsQ-dPtHWR6YiANAuiXAco6ywZm7kgOfZUYx6_3tZjyHq4-wfP6xS1Sqep7y7bm1ssVCdD2j-mJqbQwWzR8JHt7Kboc2GjlFKnD7vapgSr481KacZ6bQMyYJqk9HakkkV8kmvtq21grCehRmBew0doT7AUp3irAcrVw5KCWMmn7qwyfsg8JCwiRZVgvNcAq2XSMqQHbeywed5SRH-x_PUyASRSpT2zMfXMoZIGfvRcMkwr3N2biQjlgeyyt2gKIVVad5N60u_OF43xHr42q7toYlMvwSOcBNg2YiJx6QxL2dwu5jCjeeieqQLXo3jQdoKdjXAIPIYQnU7nzogJx_lATZyKPjQnCVyJzLLA7MtqS5Ta8dCxoqhn-Z0XSd2N8V0NsZiVj2DpJrupAX7tJjXi1ZD7GVwPvclBfa_8wcSLGrV-Df0tPseB6tk_kuCU_9VU1vzEuJTxc1j-WFflxoayh1fsxWXbjSmbqo_uRPFDtki_l0gy2Fem0kynTbPvVngiC1wZJyHlu0)
### **Client**

Сущность `Client` хранит основную информацию о клиентах CRM-системы. Используется как центральная сущность, с которой связаны задачи, встречи и сделки.

### **Task**

Сущность `Task` представляет задачу менеджера, связанную с клиентом. Используется для реализации канбан-доски и контроля выполнения задач.

### **Meeting**

Сущность `Meeting` описывает встречи и события календаря, запланированные с клиентами. Хранит временные интервалы и используется для планирования и контроля занятости.

### **Deal**

Сущность `Deal` отражает сделки, заключаемые с клиентами, и содержит финансовую информацию. Используется для анализа продаж и формирования отчётности.

### **Payment**

Сущность `Payment` хранит данные о платежах по сделкам. Поддерживает фиксацию факта оплаты, способа и статуса платежа.

## Применение основных принципов разработки
Реализация клиентского и серверного кода с учетом принципов KISS, YAGNI, DRY и SOLID В процессе рефакторинга серверной и клиентской части CRM-системы при реализации функциональности были учтены основные принципы проектирования программного обеспечения: **KISS, YAGNI, DRY и SOLID**. Ниже приведены фрагменты кода и пояснения, демонстрирующие применение каждого из принципов.

 ## 1. Принцип KISS  **Суть принципа:** Код должен быть максимально простым, понятным и не содержать избыточной логики.  Пример: обработчик команды (CQS Write) 
```public class CreateMeetingCommandHandler
    : IRequestHandler<CreateMeetingCommand, Guid>
{
    private readonly IMeetingRepository _repository;

    public CreateMeetingCommandHandler(IMeetingRepository repository)
    {
        _repository = repository;
    }

    public async Task<Guid> Handle(
        CreateMeetingCommand request,
        CancellationToken cancellationToken)
    {
        var meeting = new Meeting(
            request.ClientId,
            request.StartTime,
            request.EndTime
        );

        await _repository.AddAsync(meeting, cancellationToken);
        return meeting.Id;
    }
}
```

**Пояснение:**  
Класс выполняет только одну задачу — обработку команды создания встречи.  
Логика линейна, отсутствуют вложенные условия и избыточные абстракции, что соответствует принципу **KISS**.

----------

## 2. Принцип YAGNI

**Суть принципа:**  
Не следует реализовывать функциональность, которая не требуется на текущем этапе разработки.

### Пример: команда без лишних полей
```
public  record  CreateMeetingCommand( Guid ClientId,
    DateTime StartTime,
    DateTime EndTime ) : IRequest<Guid>;
```

**Пояснение:**  
Команда содержит только поля, необходимые для создания встречи.  
Дополнительные возможности (напоминания, участники, локация) не реализуются заранее, что соответствует принципу **YAGNI**.

----------

## 3. Принцип DRY

**Суть принципа:**  
Повторяющаяся логика должна быть вынесена в общее место и не дублироваться.

### Пример: базовый репозиторий
```
public  abstract  class  RepositoryBase<T> where  T : class { protected  readonly AppDbContext Context; protected  RepositoryBase(AppDbContext context)
    {
        Context = context;
    } public  async Task AddAsync(T entity, CancellationToken ct)
    {
        Context.Set<T>().Add(entity); await Context.SaveChangesAsync(ct);
    }
}`
```
```
public  class  MeetingRepository : RepositoryBase<Meeting>, IMeetingRepository { public  MeetingRepository(AppDbContext context)
        : base(context) { }
}
```
**Пояснение:**  
Общая логика сохранения сущностей вынесена в базовый класс.  
Это исключает дублирование кода и упрощает поддержку, что соответствует принципу **DRY**.

----------

## 4. Принципы SOLID

### 4.1. SRP — Single Responsibility Principle

**Суть принципа:**  
Каждый класс должен иметь только одну ответственность.
```
public  class  Meeting { public Guid Id { get; private  set; } public DateTime StartTime { get; private  set; } public DateTime EndTime { get; private  set; } public  Meeting(Guid clientId, DateTime start, DateTime end)
    { if (end <= start) throw  new ArgumentException("Некорректный интервал времени");

        Id = Guid.NewGuid();
        StartTime = start;
        EndTime = end;
    }
}
```
**Пояснение:**  
Сущность `Meeting` отвечает только за хранение данных и проверку своих инвариантов, что соответствует принципу **SRP**.

----------

### 4.2. OCP — Open/Closed Principle

`public  interface  INotificationPublisher { Task PublishAsync(string message);
}` 

`public  class  KafkaNotificationPublisher : INotificationPublisher { public Task PublishAsync(string message)
    { return Task.CompletedTask;
    }
}` 

**Пояснение:**  
Добавление новых способов уведомлений возможно через новые реализации интерфейса без изменения существующего кода, что соответствует принципу **OCP**.

----------

### 4.3. LSP — Liskov Substitution Principle

`public  interface  IRepository<T>
{ Task AddAsync(T entity, CancellationToken ct);
}` 

**Пояснение:**  
Любая реализация интерфейса репозитория может быть использована вместо базовой без нарушения логики работы системы, что соответствует принципу **LSP**.

----------

### 4.4. ISP — Interface Segregation Principle

`public  interface  IMeetingRepository { Task AddAsync(Meeting meeting, CancellationToken ct);
}` 

**Пояснение:**  
Интерфейс содержит только необходимые методы и не заставляет реализации зависеть от лишней функциональности, что соответствует принципу **ISP**.

----------

### 4.5. DIP — Dependency Inversion Principle
```
public  class  CreateMeetingCommandHandler { private  readonly IMeetingRepository _repository; public  CreateMeetingCommandHandler(IMeetingRepository repository)
    {
        _repository = repository;
    }
}
```
**Пояснение:**  
Класс зависит от абстракции, а не от конкретной реализации, что упрощает тестирование и соответствует принципу **DIP**.

----------

## 5. Клиентский код (KISS и DRY)

### Пример: вызов API на клиенте
```
export  async  function  createMeeting(data) { return  fetch("/api/meetings", { method: "POST", headers: { "Content-Type": "application/json" }, body: JSON.stringify(data)
  });
}
```
**Пояснение:**  
Функция выполняет одну задачу и используется повторно в разных компонентах интерфейса, что соответствует принципам **KISS** и **DRY**.

----------

## Заключение

Применение принципов **KISS, YAGNI, DRY и SOLID** при разработке клиентской и серверной части CRM-системы позволило повысить читаемость кода, упростить сопровождение, улучшить тестируемость и обеспечить готовность системы к дальнейшему расширению.

