rails g resource Account name:string payment_status:string --no-test-framework



Song
    Song belongs to an artist
    Song belongs to a genre
Artists
    Artist has many songs
    
Genres
    A Genre has many Songs


Sample Create, edit, Update
    def create
        @school_class = SchoolClass.create(params.require(:school_class).permit(:title, :room_number))
        redirect_to school_class_path(@school_class)
    end


    def edit
        @school_class = SchoolClass.find(params[:id])
    end

    def update
        @school_class = SchoolClass.find(params[:id])
        @school_class.update(params.require(:school_class).permit(:title, :room_number))
        redirect_to school_class_path(@school_class)
    end


