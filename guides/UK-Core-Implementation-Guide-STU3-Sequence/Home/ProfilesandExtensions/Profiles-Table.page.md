<fql>
from
	StructureDefinition
where
	kind = 'resource' and (status = 'active' or status = 'draft') and id.length() - id.replaceMatches('-', '').length() = 1 
select
	Profile:id, Status:status
with
  header
</fql>