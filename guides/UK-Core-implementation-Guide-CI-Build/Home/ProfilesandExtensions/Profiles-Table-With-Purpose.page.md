<fql>
from
	StructureDefinition
where
	kind = 'resource' and status = 'active' and id.length() - id.replaceMatches('-', '').length() = 1 
select
	Profile:id, Purpose:purpose, status, Resource:type
with
  no header
</fql>