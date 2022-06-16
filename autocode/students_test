package coverage

import (
	"os"
	"testing"
	"time"
)

// DO NOT EDIT THIS FUNCTION
func init() {
	content, err := os.ReadFile("students_test.go")
	if err != nil {
		panic(err)
	}
	err = os.WriteFile("autocode/students_test", content, 0644)
	if err != nil {
		panic(err)
	}
}

// WRITE YOUR CODE BELOW
func TestPeopleLen(t *testing.T) {
	var p1 = Person{
		firstName: "asd",
		lastName:  "sad",
		birthDay:  time.Time{},
	}
	var p2 = Person{
		firstName: "fef",
		lastName:  "wef",
		birthDay:  time.Time{},
	}
	people := People{p1, p2}
	if people.Len() != 2 {
		t.Errorf("Expected len is 2")
	}
}

func TestPeopleLess(t *testing.T) {
	var p1 = Person{
		firstName: "asf",
		lastName:  "sad",
		birthDay:  time.Date(2005, 8, 15, 14, 30, 45, 100, time.Local),
	}
	var p2 = Person{
		firstName: "ast",
		lastName:  "wef",
		birthDay:  time.Date(2005, 8, 15, 14, 30, 45, 100, time.Local),
	}
	var p3 = Person{
		firstName: "bds",
		lastName:  "wef",
		birthDay:  time.Date(2005, 8, 15, 14, 30, 45, 100, time.Local),
	}

	var p4 = Person{
		firstName: "bds",
		lastName:  "wef",
		birthDay:  time.Date(2004, 8, 15, 14, 30, 45, 100, time.Local),
	}

	people := People{p1, p2, p3, p4}

	isLess := people.Less(0, 1)
	isLess2 := people.Less(1, 2)
	isLess3 := people.Less(2, 3)

	if !isLess {
		t.Errorf("result shoud be true")
	}
	if !isLess2 {
		t.Errorf("should be true")
	}
	if !isLess3 {
		t.Errorf("expected true")
	}
}
func TestPeopleSwap(t *testing.T) {
	var p1 = Person{
		firstName: "asp",
		lastName:  "sad",
		birthDay:  time.Time{},
	}
	var p2 = Person{
		firstName: "fej",
		lastName:  "wef",
		birthDay:  time.Time{},
	}

	people := People{p1, p2}

	people.Swap(0, 1)

	if people.Less(0, 1) {
		t.Errorf("incorrect result found")
	}

}

func TestMatrixNew(t *testing.T) {
	m, _ := New("1 0 5 4\n 2 4 5 6")
	m2, _ := New("1 7 5 4\n 2 4 5")
	if m == nil {
		t.Errorf("incorrect resultt")
	}
	if m2 != nil {
		t.Errorf("incorrect resulttt")
	}
}

func TestMatrixRows(t *testing.T) {
	m, _ := New("1 1 5 4\n 2 4 5 6")
	if len(m.Rows()) != 2 {
		t.Errorf("incorrect result expected 2")
	}
}

func TestMatrixCols(t *testing.T) {
	m, _ := New("1 2 5 4\n 2 4 5 6")
	if len(m.Cols()) != 4 {
		t.Errorf("incorrect result expected 4")
	}
}

func TestMatrixSet(t *testing.T) {
	m2, _ := New("1 2 3 5\n 1 4 5 7")
	m2.Set(0, 0, 0)
	if m2.Rows()[0][0] != 0 {
		t.Errorf("incorrect, expected 0")
	}
	if !m2.Set(1, 0, 0) {
		t.Errorf("need true")
	}
	if m2.Set(-1, 0, 0) {
		t.Errorf("need false")
	}
}
