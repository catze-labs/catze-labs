# Backend Naming Conventions

## Folder and File convention

### Folder

Folder naming is very difficult to fix. but we use feature domain single word.
If we can't use single word, We use camel case word.

For example

- `juries`
- `auth`
- `depositHistory`

---

### File

- Dto file : `httpMethod-[whitespace to '-'].dto.ts`
- Decorator file : `name.decorator.ts`
- Filter file : `name.filter.ts`
- Controller file : `[module name].controller.ts`
- Service file : `module name.service.ts`
- Test Script file : `module name.service.spec.ts`, `[module name].controller.ts` -> `*.spec.ts`

---

## API & Host Naming

### Host Naming

{service_name}-{environment}.by-catze.xyz

e.g.

- yooldo-dev.by-catze.xyz
- yooldo-prod.by-catze.xyz
- cybergalz-dev.by-catze.xyz

---

### API URL Path Naming

Basically, Path naming form is  
<br/>
`/{version}/{domain or db table name}/{plural noun}/{singular noun}Id`

For example,

- `/v1/users/:userId`
- `/v1/juries/:juryId`
- `/v1/tokens/depositHistories/:depositHistoryId`

But, in fields, we have to define unexpected behaviors.  
So, We use form like,  
`/{version}/domain/plural noun/{singular noun}Id/[behavior to camel case]`

For example, If you want to make deny about specific withdrawal request. then,

- `/v1/tokens/withdrawalHistories/:withdrawalHistoryId/deny`

According to above example, `deny` is a behavior.

---

## AWS RDS Naming

### RDS Instance Naming

catze-{environment}-db

e.g.

- catze-cbt-db
- catze-dev-db
- catze-prod-db
- catze-qa-db
- catze-stage-db

---

### Database naming

{service_name}

e.g.

- yooldo
- cybergalz
- backoffice

e.g.

- cybergalz-dev
