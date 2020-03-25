import java.util.List;

import javax.ws.rs.GET;
import javax.ws.rs.POST;
import javax.ws.rs.Path;
import javax.ws.rs.PathParam;
import javax.ws.rs.Produces;
import javax.ws.rs.core.MediaType;

@Path("crews")
public class SchoolResource {

	SchoolRepository repo = new SchoolRepository();
	
	@GET
	@Produces({MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML})
	public List<School> getCrews() {
		System.out.println("getSchool called...");
		return repo.getCrews();
	}
	
	@GET
	@Path("crew={id}")
	@Produces({MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML})
	public School getCrew(@PathParam("id") int id) {
		return repo.getCrew(id);
	}
	
	@POST
	@Path("crew")
	public School createCrew(Polytec a1) {
		System.out.println(a1); 
		repo.create(a1);
		
		return a1;
	}
}
