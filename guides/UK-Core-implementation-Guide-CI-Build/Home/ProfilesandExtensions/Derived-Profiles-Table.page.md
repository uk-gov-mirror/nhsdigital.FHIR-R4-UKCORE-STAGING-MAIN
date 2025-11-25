<fql>
from
	StructureDefinition
where
	kind = 'resource' and status = 'active' and id.length() - id.replaceMatches('-', '').length() > 1 
select
	Profile:id, status
with
  no header
</fql>
