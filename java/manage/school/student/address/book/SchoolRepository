import java.util.ArrayList;
import java.util.List;

public class SchoolRepository {
	List<Polytec> crews;
	
	public SchoolRepository() {
		crews = new ArrayList<>();
		
		School a1 = new School();
		a1.setId(101);
		a1.setName("Gwanzo");
		a1.setPoints(60);
		
		School a2 = new School(); 
		a2.setId(102);
		a2.setName("Siilver9");
		a2.setPoints(70);
		
		School a3 = new School(); 
		a3.setId(103);
		a3.setName("Elon Musk");
		a3.setPoints(80);
		
		crews.add(a1);
		crews.add(a2);
		crews.add(a3);

	}
	
	public List<School> getCrews(){
		
		return crews;
	}
	
	
	public School getCrew(int id) {
		
		for(School a : crews) {
			if(a.getId()==id) {
				return a;
			}
		}
		
		return new School();
	}

	public void create(School a1) {
		// TODO Auto-generated method stub
		crews.add(a1);
	}
}
